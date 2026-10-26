# 7. Webhooks (FP 2602+)

> Source: *Working with SAP Business One Service Layer* v1.29, chapter 7 (paraphrased technical reference).
>
> **Resumen (ES):** notificaciones instantáneas a un endpoint HTTPS propio cuando ocurren eventos en SAP B1 (crear/actualizar/cerrar/cancelar objetos). Cubre habilitación, catálogo de eventos, suscripciones (`EventSubscriptions`), handshake y autenticación, notificaciones (`EventNotifications`) y su payload, configuración, Webhook Messenger, fórmulas de filtro y FAQ.

Available since **SAP Business One 10.0 FP 2602**. A new component, the **Webhook Messenger Service**, runs as a daemon behind Service Layer (per service unit) and delivers the notifications. **Use OData v4 (`/b1s/v2/`) for every webhook API.**

## 7.1 Quick start

1. **Enable webhooks for the company** (disabled by default):

   ```http
   POST /b1s/v2/CompanyService_UpdateAdminInfo
   { "AdminInfo": { "EnableWebhook": "tYES" } }
   ```

2. **Expose an endpoint** in your app (for tests, a sample service or https://webhook.site).
3. **Create a subscription**:

   ```http
   POST /b1s/v2/EventSubscriptions
   { "WebhookID": "MyWebhook",
     "WebhookURL": "https://partner-webhook-service:3000/MyWebhook",
     "AuthenticationType": "None",
     "Handshake": "tNO",
     "EventCollection": [ { "BusinessObject": "Orders", "TransactionType": "Created" } ] }
   ```

4. Make sure the **Webhook Messenger Service** is installed and running.
5. **Trigger the event** (e.g. create a sales order from SL, DI API, the desktop client or the Web Client).
6. **Verify** your endpoint receives and processes the notification.

## 7.2 Event catalog

Lists the events you can subscribe to, by business object and transaction type — includes system objects, **UDOs and UDTs**:

```http
GET /b1s/v2/EventSubscriptionsService_GetEventCatalog
```

```json
{ "Version": "1.0", "Description": "SAP Business One Event Catalog",
  "value": [
    { "BusinessObject": "BusinessPartners", "ObjectType": "2",    "TransactionTypes": "Created,Updated,Deleted" },
    { "BusinessObject": "Orders",           "ObjectType": "17",   "TransactionTypes": "Created,Updated,Deleted,Closed,Cancelled,Reopened" },
    { "BusinessObject": "Activities",       "ObjectType": "1007", "TransactionTypes": "Created,Updated,Deleted" }, ... ] }
```

## 7.3 Event subscriptions — entity `EventSubscriptions` (key `WebhookID`)

### Operations

| Operation | Request | Notes | Operación (ES) |
|---|---|---|---|
| Create | `POST EventSubscriptions` + JSON | Handshake runs automatically if `Handshake: tYES`; if it fails the webhook isn't created | Crear |
| List | `GET EventSubscriptions` | | Listar |
| Get one | `GET EventSubscriptions('MyWebhook')` | | Obtener |
| Filter | `GET EventSubscriptions?$filter=AuthenticationType eq 'HMAC'` | | Filtrar |
| Add events | `PATCH EventSubscriptions('MyWebhook')` `{"EventCollection": [ {"BusinessObject": "Invoices", "TransactionType": "Updated"} ]}` | PATCH **appends** to the collection | Agregar eventos |
| Replace / remove events | `PATCH EventSubscriptions('MyWebhook')` + header **`B1S-ReplaceCollectionsOnPatch: true`** with the full desired `EventCollection` | Full replacement of the collection | Reemplazar/quitar eventos |
| Delete | `DELETE EventSubscriptions('MyWebhook')` | | Borrar |
| Resume | `POST EventSubscriptions('MyWebhook')/Resume` → `204` | Reactivates a webhook deactivated by errors (handshake runs if enabled; on failure stays inactive) | Reanudar |
| Pause | `POST EventSubscriptions('MyWebhook')/Pause` → `204` | Stops notifications until resumed | Pausar |
| Handshake | `POST EventSubscriptions('MyWebhook')/Handshake` → `204` or error | Manual verification | Handshake manual |
| Replay | `POST EventSubscriptions('MyWebhook')/Replay` → `204` | Resends **all missed notifications since the last successful delivery**. Requires the webhook to be **Inactive** and to support handshake. Work mode goes to `Replay`, then back to `Standard`. **While replaying, the messenger stops sending new notifications to all other webhooks** | Reenviar perdidos |

Full create example (HMAC + handshake):

```json
POST /b1s/v2/EventSubscriptions
{ "WebhookID": "MyWebhook",
  "WebhookURL": "https://partner-webhook-service:3000/MyWebhook",
  "AuthenticationType": "HMAC",
  "AuthenticationCred": "{\"Key\": \"i1mGRbx8DaYZQ6p7RJywYD1IauI+HyTj4TjyKSYv8sI=\", \"Algorithm\": \"hmacsha256\"}",
  "Handshake": "tYES",
  "VerifyCertificate": "tYES",
  "EventCollection": [ { "BusinessObject": "Activities", "TransactionType": "Updated" },
                       { "BusinessObject": "Orders", "TransactionType": "Created" } ] }
```

### 7.3.1.1 Handshake

1. B1 generates a random **token** per handshake.
2. Sends `GET <WebhookURL>` with header **`X-B1-Webhook-Token: <token>`** (plus auth headers if configured).
3. Your endpoint must answer with body **`{"Challenge": "<token>"}`**.
4. B1 validates the echo → webhook confirmed.

Your endpoint must therefore support **GET**, read the custom header and reply in that format.

Automatic handshakes: on creation (if `Handshake: tYES`) and on `Resume`.

Headers sent per authentication type:

| AuthenticationType | Extra header on handshake/notifications | Cabecera (ES) |
|---|---|---|
| None | only `X-B1-Webhook-Token` (handshake) | Ninguna |
| Basic | `Authorization: Basic base64(username:password)` | Básica |
| OAuth | `Authorization: Bearer <access_token>` (client-credentials flow against your token endpoint) | OAuth |
| HMAC | `X-B1-Webhook-Signature: <signature>` — HMAC of the token (handshake) using the key/algorithm in `AuthenticationCred` | Firma HMAC |

### 7.3.2 EventSubscription properties

| Property | Type | Required | Description | Default | Descripción (ES) |
|---|---|---|---|---|---|
| `WebhookID` | String | Yes | Unique ID in the company, non-empty | — | ID único |
| `WebhookURL` | String | Yes | Valid, unique in the company, **HTTPS only** | — | URL HTTPS del endpoint |
| `AuthenticationType` | String | No | `None`, `Basic`, `HMAC`, `OAuth`. If not `None`, `AuthenticationCred` is required | `HMAC` | Tipo de autenticación |
| `AuthenticationCred` | String (JSON text) | If auth ≠ None | Basic: `{"Username": "partner1", "Password": "12345"}`; HMAC: `{"Key": "my_secret_key", "Algorithm": "HMACSha256"}` (`HMACSha256` / `HMACSha384` / `HMACSha512`); OAuth: `{"token_endpoint": "https://auth.example.com/oauth2/token", "client_id": "...", "client_secret": "...", "grant_type": "client_credentials"}` | — | Credenciales |
| `VerifyCertificate` | `tYES`/`tNO` | No | Validate the endpoint's SSL certificate (keep `tYES` in production) | `tYES` | Verificar certificado SSL |
| `State` | String | Yes | `Active` (receives), `Inactive` (doesn't), `Exceptional` (delivery problems; retried — returns to Active if fixed within the max retries, otherwise becomes Inactive) | `Active` | Estado |
| `WorkMode` | String | Yes | `Standard` (missed notifications during downtime are ignored) or `Replay` (sending missed notifications; only via Replay API) | `Standard` | Modo de trabajo |
| `Handshake` | `tYES`/`tNO` | No | Require handshake verification (keep `tYES` in production) | `tYES` | Requiere handshake |
| `EventCollection` | Array | Yes (≥ 1) | Events subscribed, see below | — | Eventos suscriptos |

Event object (inside `EventCollection`):

| Field | Required | Description | Descripción (ES) |
|---|---|---|---|
| `BusinessObject` | Yes | SL entity set name (e.g. `Orders`, `Invoices`) | Objeto de negocio |
| `TransactionType` | Yes | Must exist in the catalog for that object (e.g. `Created`, `Updated`, `Deleted`, `Closed`, `Cancelled`, `Reopened`) | Tipo de transacción |
| `BizObjProps` (FP 2608+) | No | Comma-separated **simple** properties to add to the payload (default: only key fields). Complex properties (lines, prices) not allowed. E.g. `"DocEntry, CardCode, DocTotal"` | Propiedades extra |
| `FilterExpr` (FP 2608+) | No | Boolean formula; only matching events are notified (see 7.7). E.g. `"DocTotal > 1000"`, `"DocDueDate -- DocDate < 7"` | Filtro |

### 7.3.3 Permissions

- Normal users get `403 Forbidden` by default.
- Grant in the B1 client: **General Authorizations → Webhook Manipulation** → *Full Authorization* or *Read-Only*.
- Programmatically (superuser), permission ID **2249**:

  ```http
  POST /b1s/v2/SBOBobService_SetSystemPermission
  { "PermissionID": "2249", "UserCode": "user1", "Permission": 1 }
  ```

- Superusers have full rights; changes may take ~1 minute (permission cache).

## 7.4 Event notifications

When a subscribed event occurs, the messenger **POSTs** to `WebhookURL`. Each dispatched notification is stored and can be queried (read-only) through **`EventNotifications`**.

```http
GET /b1s/v2/EventNotifications?$filter=BusinessObject eq 'Orders' and Operation eq 'Created'&$top=10&$orderby=CreateTime desc
GET /b1s/v2/EventNotifications('3f03e9da-8dd6-4601-be18-5cad6790bfd3')
```

Create/update/delete on `EventNotifications` are **not** supported (managed by B1 core and the messenger).

### EventNotifications properties

| Property | Type | Description | Example | Descripción (ES) |
|---|---|---|---|---|
| `EventID` | String (GUID) | Unique notification ID | `3f03e9da-8dd6-4601-be18-5cad6790bfd3` | ID del evento |
| `SourceDB` | String | Company DB where the event occurred | `SBODEMOUS` | Base de origen |
| `BusinessObject` | String | Affected object (same name as in the subscription) | `Orders` | Objeto |
| `Operation` | String | Transaction type | `Created` | Operación |
| `Status` | String | `New`, `Delivered`, `Failed`, `PartiallyDelivered`, `Archived` (default `New`) | `New` | Estado de entrega |
| `ReplayState` | String | `None`, `Replaying`, `Completed` (default `None`) | `None` | Estado de reenvío |
| `FieldNames` | String | Comma-separated key field names (tab-separated for multi-key) | `DocEntry`; `CardCode`; `CardCode	ItemCode` (SpecialPrices) | Campos clave |
| `FieldValues` | String | Matching values | `91`; `C20000` | Valores |
| `CreateDate` | Date | `yyyy-MM-ddT00:00:00Z` | `2025-11-19T00:00:00Z` | Fecha |
| `CreateTime` | String | `HH:mm:ss.fff` (24 h) | `16:45:21.907` | Hora |
| `KeyData` (FP 2608+) | JSON string | Key as JSON | `{"DocEntry": 91}`, `{"CardCode": "C20000"}` | Clave en JSON |
| `DeliveryDetails` (FP 2608+) | Collection | Per webhook: WebhookID, delivery status, attempts, last attempt time, HTTP response code | | Detalle de entregas |
| `ExtDataList` (FP 2608+) | Collection | Per webhook: WebhookID, JSON of extra data (BizObjProps), value of the filter expression | | Datos adicionales |

### 7.4.2 Payload (SAP Events / CloudEvents-style)

| Field | Meaning | Significado (ES) |
|---|---|---|
| `id` | Unique notification ID | ID único |
| `specversion` | SAP Events spec version (`1.0`) | Versión de la especificación |
| `source` | Origin, e.g. `/default/sap.b1/DEMODB1` | Origen (sistema/sociedad) |
| `type` | `sap.b1.{BusinessObject}.{Operation}.v1`, e.g. `sap.b1.Orders.Created.v1` | Tipo de evento |
| `subject` | Usually the primary key (e.g. `"91"`) | Clave del objeto |
| `time` | UTC ISO 8601 timestamp | Momento del evento |
| `datacontenttype` | `application/json` | Tipo de contenido |
| `data` | Key fields + optional `BizObjProps` | Datos |

Notifications are sent **in batches by default** (always a JSON array); batch size = `MessageBatchLimit`.

```json
[ { "id": "5ac18923-cfce-40d3-a31e-7154ca4d5191", "specversion": "1.0",
    "source": "/default/sap.b1/DEMODB1", "type": "sap.b1.Orders.Created.v1",
    "subject": "91", "time": "2025-11-10T23:10:22.917Z",
    "datacontenttype": "application/json",
    "data": { "DocEntry": 91, "CardCode": "C20000", "DocTotal": 1500.00 } } ]
```

## 7.5 Company-level configuration (AdminInfo)

| Option | Type | Default | Description | Opción (ES) |
|---|---|---|---|---|
| `EnableWebhook` | `tYES`/`tNO` | `tNO` | Turn webhooks on | Habilitar webhooks |
| `MaxNumberOfWebHooks` | Integer | 16 | Max webhooks per company | Máximo de webhooks |
| `MessageTTL` | Integer (hours) | 24 | Older messages are discarded; keep well below `MessageRetentionTime` | Vida de los mensajes |
| `WebhookRetryTimes` | Integer | 3 | Retries on failure (0 = none) | Reintentos |
| `WebhookRetryInterval` | Integer (s) | 2 | Interval between retries | Intervalo de reintentos |
| `WebhookRequestTimeout` | Integer (s) | 10 | Timeout per notification request | Timeout |
| `MessageBatchLimit` | Integer | 1024 | Max messages per request (tune to the receiver) | Tamaño de lote |
| `MessageRetentionTime` | Integer (days) | 30 | Days messages are stored before deletion | Retención |

```http
POST /b1s/v2/CompanyService_UpdateAdminInfo
{ "AdminInfo": { "EnableWebhook": "tYES", "MaxNumberOfWebHooks": 20, "MessageBatchLimit": 32 } }

GET /b1s/v2/CompanyService_GetAdminInfo
```

If `UpdateAdminInfo` fails with **`10001237 - Enter valid folder path`**, a folder in AdminInfo (e.g. `ExcelFolderPath`, `XMLFileFolderPath`) doesn't exist on the SL server or SL lacks permissions. Fix the folders, or (if unused) blank them: `{"AdminInfo": {"EnableWebhook": "tYES", "ExcelFolderPath": "", "XMLFileFolderPath": ""}}`.

## 7.6 Webhook Messenger

| Feature | Description | Característica (ES) |
|---|---|---|
| Asynchronous | Doesn't block the B1 core | Asíncrono |
| Retries | Per configured policy | Reintentos |
| Batching | Several notifications per request | Lotes |
| Security | SSL verification; Basic/HMAC/OAuth | Seguridad |
| Ordering | In event order **within one company**; not guaranteed across companies | Orden |
| Deactivation | Webhooks failing repeatedly are deactivated; reactivate with Resume | Desactivación |
| Handshake / Replay | Supported (replay is manual and pauses other webhooks) | Handshake / reenvío |

- **Health check:** `telnet <messenger host> 40008` (default port **40008**).
- **Self-signed / untrusted certificates:** import them with the certificate import tool (PowerShell/shell script) in the messenger's `tools` folder, e.g. `C:\Program Files\SAP\SAP Business One Webhook Messenger\tools` (run with `--help` as administrator).

## 7.7 Webhook formula (`FilterExpr`, FP 2608+)

Boolean expressions over the business object's fields.

| Element | Syntax / examples | Elemento (ES) |
|---|---|---|
| Literals | numbers `3`, `45.6`, `-20`; strings `'hello'`; booleans | Literales |
| Variables | Business object properties (e.g. `DocTotal`, `CardCode`) | Variables (campos) |
| Relational | `==`, `!=`, `>`, `<`, `>=`, `<=` — e.g. `1+2 >= 3`, `CardCode != CardName` | Comparación |
| Logical | `||`, `&&`, `!` — e.g. `DocEntry > 1024 && CardCode != CardName || DocTotal <= 1000` | Lógicos |
| Parentheses | `DocNum > DocEntry && (DocDueDate >= DocDate || DocTotal <= 1000)` | Paréntesis |
| Arithmetic | `+ - * /` — `100 + Quantity * UnitPrice * 0.1` | Aritméticos |
| String `+` | Concatenation; numbers converted silently: `CardCode + " and " + CardName`, `'abc' + 1 == 'abc1'` | Concatenación |
| Date ops | `DocDueDate + 5` (add days), `DocDueDate - 5`, days between: `DocDueDate -- DocDate`, constant `DATE(2026, 7, 28)` | Operaciones con fechas |
| Time ops | `StartTime + 300` (seconds), `StartTime - 300`, seconds between: `EndTime -- StartTime`, constant `TIME(19, 28, 59)` | Operaciones con horas |

Functions:

| Category | Function | Example → result | Categoría (ES) |
|---|---|---|---|
| String | `UPPER(text)` | `UPPER("abcABC")` → `'ABCABC'` | Texto |
| String | `LOWER(text)` | `LOWER("abcABC")` → `'abcabc'` | Texto |
| String | `CONTAINS(text, compare_text)` | `CONTAINS('abcABC','ABC')` → true | Texto |
| String | `TRIM(text)` | `TRIM(' Hello World ')` → `'Hello World'` | Texto |
| String | `LEN(text)` | `LEN('Hello World')` → 11 | Texto |
| String | `LEFT(text, n)` / `RIGHT(text, n)` | `LEFT('Hello World', 5)` → `'Hello'`; `RIGHT(...,5)` → `'World'` | Texto |
| String | `MID(text, start, n)` (1-based; numeric strings accepted) | `MID('Hello World', 6, 5)` → `'World'`; `MID('Sample', 2, 10)` → `'mple'` | Texto |
| String | `SUBSTITUTE(text, old, new)` | `SUBSTITUTE('banana','a','o')` → `'bonono'` (empty `old` → unchanged) | Texto |
| Date | `DATE(y, m, d)` (1970–9999) | `DATE(2020, 2, 28) + 1` → `DATE(2020, 2, 29)` | Fecha |
| Date | `TODAY()` | current local date | Fecha |
| Date | `YEAR/MONTH/DAY(date or 'YYYYMMDD')` | `YEAR('20000101')` → 2000; `DAY(DATE(2026,7,17))` → 17 | Fecha |
| Time | `TIME(h, m, s)` (24 h) | `TIME(23, 59, 59) + 1` → `TIME(0, 0, 0)` | Hora |
| Time | `NOW()` | current local time | Hora |
| Time | `HOUR/MINUTE/SECOND(time or 'HHMMSS'/'HHMM')` | `HOUR('2359')` → 23; `SECOND('2359')` → 0 | Hora |
| Math | `ABS(x)` | `ABS(-10)` → 10 | Matemática |
| Math | `FLOOR(x)` | `FLOOR(-4.5)` → -5 | Matemática |
| Math | `CEILING(x)` | `CEILING(-4.5)` → -4 | Matemática |
| Math | `ROUND(x)` | `ROUND(4.5)` → 5; `ROUND(-4.5)` → -4 | Matemática |
| Math | `MIN(e1, ...)`, `MAX(e1, ...)` (numbers or strings) | `MAX(3,5,7)` → 7; `MIN('a','b')` → `'a'` | Matemática |
| Logical | `IFNULL(expr, alt)` | `IFNULL(null, 'default')` → `'default'` | Lógica |

App-level variables (`app.` namespace):

| Variable | Returns | Example | Variable (ES) |
|---|---|---|---|
| `app.CurrentUser` | Logged-in user code | `'manager'` | Usuario actual |
| `app.CurrentCompany` | Company name | `'SQLTA OEC Computers'` | Sociedad actual |
| `app.Name` | Process name without extension | `'SAP Business One'` (desktop) / `'httpd'` (Service Layer) | Proceso |
| `app.VersionStr` | Application version | `'10.00.340'` | Versión |
| `app.OS` | OS | `'WIN'` or `'LINUX'` | Sistema operativo |

## 7.8 FAQ

| Question | Answer | Respuesta (ES) |
|---|---|---|
| When does the messenger retry? | On HTTP **5xx** (500, 502, 503, 504), **408**, **429**, and network errors (timeouts, connection refused, DNS failures) | Reintenta en 5xx, 408, 429 y errores de red |
| Retry policy? | Up to **five retries with exponential backoff**: 2 s, 4 s, 8 s, 16 s, 32 s; then the notification is marked failed (per the FAQ; the AdminInfo defaults are `WebhookRetryTimes=3`, `WebhookRetryInterval=2`) | Backoff exponencial |
| Ordered delivery? | Within one company yes (even with retries); not across companies → design receivers to tolerate out-of-order events | Orden por sociedad |
| Duplicates? | One notification per event, but retries can duplicate → make the receiver **idempotent** using `id` | Puede haber duplicados: ser idempotente |
| Typical URL validation errors | Not HTTPS / malformed URL (`http://...`, `https://webhook`, `https://256.256.256.256/...`); connection refused (service down, port blocked); **SSL certificate doesn't match host/IP** (SAN must include the IP — enforced even with `VerifyCertificate=tNO`); timeout (> 10 s default); untrusted certificate with `VerifyCertificate=tYES`. On these errors the webhook is **deactivated** until Resume | Errores de validación de la URL |
| Retry vs. replay | Retry = automatic resend of one failed notification; Replay = manual API that resends everything missed during downtime | Reintento vs. reenvío |
| Endpoint best practices | High availability/failover, robust error handling and logging, handle retries/duplicates, test regularly, monitor performance | Buenas prácticas |
| Slow endpoint / backlog | Notifications are queued in memory; when full, the messenger waits; batching mitigates slow receivers | Endpoint lento |
| Error 10001237 when enabling | Invalid folder paths in AdminInfo (see 7.5) | Error 10001237 |
