# 3.4–3.5 CRUD Operations and Actions

> Source: *Working with SAP Business One Service Layer* v1.29, sections 3.4–3.5 (paraphrased technical reference).
>
> **Resumen (ES):** cómo crear, leer, actualizar y borrar entidades, cómo crear sin devolver contenido, y cómo invocar acciones ligadas (bound) y globales (servicios), incluida la vista previa de documentos.

## Summary table

| Operation | HTTP | URL pattern | Success code | Operación (ES) |
|---|---|---|---|---|
| Create | `POST` | `/EntitySet` + JSON body | `201 Created` (body = created entity) or `204` with `Prefer: return-no-content` | Crear |
| Retrieve one | `GET` | `/EntitySet(key)` | `200 OK` | Leer una entidad |
| Retrieve collection | `GET` | `/EntitySet?query options` | `200 OK` (paged) | Leer colección |
| Update (partial) | `PATCH` | `/EntitySet(key)` + changed fields | `204 No Content` | Actualizar parcial (recomendado) |
| Update (full) | `PUT` | `/EntitySet(key)` + full body | `204 No Content` | Reemplazar (campos omitidos → valor por defecto/null) |
| Delete | `DELETE` | `/EntitySet(key)` | `204 No Content` | Borrar |
| Bound action | `POST` | `/EntitySet(key)/Action` | `204`/`200` | Acción sobre una entidad |
| Global action (service) | `POST` | `/XxxService_Method` + JSON params | `200`/`204` | Acción global (servicio) |

## 3.4.1 Creating entities

Create a customer:

```http
POST /BusinessPartners
{ "CardCode": "c1", "CardName": "customer c1", "CardType": "cCustomer" }
```

- Valid fields are those of the entity type (`SAPB1.BusinessPartner`).
- **Enums accept either the name or the stored value**: `"CardType": "cCustomer"` ≡ `"CardType": "C"`.
- Success: `201 Created` with the full entity (including defaults such as `GroupCode`).
- Error example (duplicate code):

```json
HTTP/1.1 400 Bad Request
{ "error": { "code": -10, "message": { "lang": "en-us",
  "value": "1320000140 - Business partner code 'c1' already assigned to a business partner; enter a unique business partner code" } } }
```

Create a sales order with two lines (`DocumentLines` is a collection of `DocumentLine`, i.e. a JSON array):

```http
POST /Orders
{
  "CardCode": "c1", "DocDate": "2014-04-01", "DocDueDate": "2014-04-01",
  "DocumentLines": [
    { "ItemCode": "i1", "UnitPrice": 100, "Quantity": 10, "TaxCode": "T1" },
    { "ItemCode": "i2", "UnitPrice": 120, "Quantity": 8,  "TaxCode": "T1" }
  ]
}
```

Response `201 Created` with `DocEntry`, `DocNum`, `DocType` and the lines with their `LineNum` (0, 1, …).

## 3.4.2 Retrieving entities

| Case | Request | Caso (ES) |
|---|---|---|
| String key | `GET /BusinessPartners('c1')` or `GET /BusinessPartners(CardCode='c1')` | Clave texto: con comillas simples |
| Integer key | `GET /Orders(22)` or `GET /Orders(DocEntry=22)` | Clave numérica: sin comillas |
| Composite key | `GET /SalesTaxAuthorities(Code='AK',Type=-3)` | Clave compuesta |

Strings need single quotes; integers must not have them.

## 3.4.3 Updating entities

```http
PATCH /BusinessPartners('c1')
{ "CardName": "Updated customer name" }
```

- `PATCH` keeps properties not sent; `PUT` resets omitted properties to default/null → **use PATCH**.
- Read-only properties (e.g. `CardCode`) are silently ignored.
- Success: `204 No Content`.

## 3.4.4 Deleting entities

```http
DELETE /BusinessPartners('c1')     → 204 No Content
```

Some objects can't be deleted (same rules as the B1 client). Deleting a sales order:

```json
DELETE /Orders(22)
HTTP/1.1 400 Bad Request
{ "error": { "code": -5006, "message": { "lang": "en-us", "value": "The requested action is not supported for this object." } } }
```

For documents use **Cancel/Close** actions instead.

## 3.4.5 Create without returning content

For high-throughput scenarios, ask the server not to return the created entity:

```http
POST /b1s/v1/Items
Prefer: return-no-content

{ "ItemCode": "i011" }
```

```http
HTTP/1.1 204 No Content
Location: /b1s/v1/Items('i011')
Preference-Applied: return-no-content
```

`Preference-Applied` confirms the preference was honored; `Location` holds the URI of the new resource.

## 3.5 Actions

| Kind | Purpose | URL | Tipo (ES) |
|---|---|---|---|
| Bound action | Operation on a specific entity other than CRUD (Close, Cancel, Reopen, …) | `POST /Orders(22)/Close` | Acción ligada a una entidad |
| Global action | Exposes B1 **services** (CompanyService, SeriesService, …) and utilities | `POST /ActivitiesService_AddActivity` | Acción global (servicios) |

- Request/response types are described in the metadata.
- "Action" is the OData v4 term; in OData v3 the same thing is a **FunctionImport**.
- Always invoked with **POST**.

### Bound action example

```xml
<Action IsBindable="true" Name="Close"><Parameter Name="Document" Type="SAPB1.Document"/></Action>
```

Orders are of type `Document`, so: `POST /Orders(22)/Close`.

### Global action example (service)

Metadata (OData v4):

```xml
<Action Name="ActivitiesService_GetActivity">
  <Parameter Name="ActivityParams" Type="SAPB1.ActivityParams"/>
  <ReturnType Type="SAPB1.Activity"/>
</Action>
<Action Name="ActivitiesService_AddActivity">
  <Parameter Name="Activity" Type="SAPB1.Activity"/>
  <ReturnType Type="SAPB1.ActivityParams"/>
</Action>
```

Calls — **the body wraps the payload in an object named after the parameter**:

```http
POST /ActivitiesService_AddActivity
{ "Activity": { "ActivityCode": 1, "CardCode": "c1" } }

POST /ActivitiesService_GetActivity
{ "ActivityParams": { "ActivityCode": 1 } }
```

`AddActivity` returns `ActivityParams`; `GetActivity` returns `Activity`. Since 9.1 PL02, `Activities` is exposed as an entity set, so these global actions are hidden by default.

### Previewing a document (hidden action `OrdersService_Preview`)

Simulates creation without saving (taxes, totals, defaults, accounts are calculated):

```http
POST /b1s/v1/OrdersService_Preview
{ "Document": { "CardCode": "c1", "DocDate": "2014-04-01", "DocDueDate": "2014-04-01",
   "DocumentLines": [ { "ItemCode": "i1", "UnitPrice": 100, "Quantity": 10, "TaxCode": "" } ] } }
```

Returns `200 OK` with the computed document: `DocEntry`/`DocNum` are `null`, plus `DocTotal`, `DocCurrency`, `JournalMemo`, `DocumentStatus: bost_Open`, and each line with `Price`, `PriceAfterVAT`, `WarehouseCode`, `AccountCode`, `LineTotal`, `TaxTotal`, `UoMCode`, `InventoryQuantity`, etc. (Every marketing-document service exposes a similar `XxxService_Preview` operation — see the *Servicios* docs.)
