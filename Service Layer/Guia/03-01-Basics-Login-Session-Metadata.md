# 3.0–3.3 Basics, Login/Logout, Session, Metadata and Service Document

> Source: *Working with SAP Business One Service Layer* v1.29, sections 3 – 3.3 (paraphrased technical reference).
>
> **Resumen (ES):** elementos de una URL del Service Layer, cómo iniciar/cerrar sesión, cookies de sesión, documento de metadatos (incluida la consulta de metadatos con anotaciones OData v4) y documento de servicio.

## Key URL elements

| Element | Description | Example | Descripción (ES) |
|---|---|---|---|
| Service root URL | Root of the API. HTTPS by default | `https://<server>:<port>/b1s/<version>` e.g. `https://dbserver:50000/b1s/v1` (OData v3) or `/b1s/v2` (OData v4) | URL raíz del servicio |
| Resource path | Collection or single entity to act on | `https://dbserver:50000/b1s/v1/Items` | Ruta del recurso (colección o entidad) |
| Query options | Options/parameters appended to the URL | `.../Items?$top=2&$orderby=itemcode` | Opciones de consulta |
| HTTP verb | Action on the resource (REST): GET, POST, PATCH, PUT, DELETE | `POST https://dbserver/b1s/v1/Login` ≡ `POST /Login` (relative form used in examples) | Verbo HTTP |
| JSON representation | Body of requests/responses | `{"key1":"value1","arr1":[100,200]}` | Cuerpo JSON |

Tip from the guide: to try SL without writing code, use **Postman** (or an equivalent REST client).

## 3.1 Login and Logout

Every operation requires a session. Login:

```http
POST https://<server>:<port>/b1s/v1/Login
Content-Type: application/json

{"CompanyDB": "US506", "UserName": "manager", "Password": "1234"}
```

Successful response:

```http
HTTP/1.1 200 OK
Set-Cookie: B1SESSION=PTRzIjYK-weN6-1Lx1-ZG0J-3ARxfjcU0Shy;HttpOnly;
Set-Cookie: ROUTEID=.node1; path=/b1s

{
  "odata.metadata": "https://dbserver:50000/b1s/v1/$metadata#B1Sessions/@Element",
  "SessionId": "PTRzIjYK-weN6-1Lx1-ZG0J-3ARxfjcU0Shy",
  "Version": "1000110",
  "SessionTimeout": 30
}
```

| Cookie / field | Meaning | Significado (ES) |
|---|---|---|
| `B1SESSION` | Session ID set by Service Layer. **Mandatory** on every subsequent request | ID de sesión; obligatorio en cada request |
| `ROUTEID` | Set by Apache for load-balancer stickiness (e.g. `.node1`). Optional, but improves performance | Afinidad con el nodo; opcional pero recomendado |
| `SessionTimeout` | Minutes of inactivity before the session expires (30 by default) | Minutos de inactividad antes de expirar |
| `Version` | Service Layer / B1 version | Versión |

Since **SAP Business One 10.0 FP2305** you can log in with a **Windows domain account** once Active Directory Domain Services is activated and its users are bound to company users (see *Identity and Authentication Management in SAP Business One*, section *SL Connection References*).

Logout:

```http
POST /Logout
Cookie: B1SESSION=PTRzIjYK-weN6-1Lx1-ZG0J-3ARxfjcU0Shy; ROUTEID=.node1
```

Response: `HTTP/1.1 204 No Content`.

### 3.1.1 Session

- A session starts with `Login` and ends with `Logout`; each one has a unique GUID-like ID.
- Send the cookie on every call:

```http
GET /Items('i001')
Cookie: B1SESSION=PTRzIjYK-weN6-1Lx1-ZG0J-3ARxfjcU0Shy; ROUTEID=.node1
```

- Desktop/server applications (not browser) **must add the cookie header manually**; otherwise you get:

```json
HTTP/1.1 401 Unauthorized
{ "error": { "code": 301, "message": { "lang": "en-us", "value": "Invalid session or session already timeout." } } }
```

- JavaScript running in a browser (Browser Access) does not need to set the cookie manually — the browser handles it.

## 3.2 Metadata document

Metadata describes the service: **types, entities (B1 objects) and actions (B1 services)**.

```http
GET /$metadata
```

Example fragments (business partners and orders):

```xml
<!-- 1.1 enum -->
<EnumType Name="BoCardTypes">
  <Member Name="cCustomer" Value="C"/> <Member Name="cSupplier" Value="S"/> <Member Name="cLid" Value="L"/>
</EnumType>
<!-- 1.2 entity type -->
<EntityType Name="BusinessPartner">
  <Key><PropertyRef Name="CardCode"/></Key>
  <Property Name="CardCode" Nullable="false" Type="Edm.String"/>
  <Property Name="CardName" Type="Edm.String"/>
  <Property Name="CardType" Type="SAPB1.BoCardTypes"/> ...
</EntityType>
<!-- 1.3 parameter complex type -->
<ComplexType Name="DocumentParams"><Property Name="DocEntry" Nullable="false" Type="Edm.Int32"/></ComplexType>
<!-- 1.4 document entity -->
<EntityType Name="Document">
  <Key><PropertyRef Name="DocEntry"/></Key>
  <Property Name="DocEntry" Nullable="false" Type="Edm.Int32"/>
  <Property Name="DocumentLines" Type="Collection(SAPB1.DocumentLine)"/> ...
</EntityType>
<!-- 1.5 line complex type -->
<ComplexType Name="DocumentLine"> <Property Name="LineNum" .../> <Property Name="ItemCode" .../> ... </ComplexType>
<!-- 2 bound action -->
<Action IsBindable="true" Name="Close"><Parameter Name="Document" Type="SAPB1.Document"/></Action>
<!-- 3 container -->
<EntityContainer Name="ServiceLayer">
  <EntitySet EntityType="SAPB1.BusinessPartner" Name="BusinessPartners"/>
  <EntitySet EntityType="SAPB1.Document" Name="Orders"/> ...
</EntityContainer>
```

How to read it:

| Metadata element | What it tells you | Qué indica (ES) |
|---|---|---|
| `EntitySet` (in `EntityContainer`) | An exposed collection you can CRUD (e.g. `BusinessPartners`, `Orders`) | Colección expuesta con CRUD |
| `EntityType` | Structure + key of the entity (e.g. `Document` is shared by Orders, Invoices, …) | Estructura y clave |
| `ComplexType` | Sub-objects/lines (e.g. `DocumentLine`) and parameter types (`...Params`) | Sub-objetos, líneas y parámetros |
| `EnumType` | Allowed values (name and value both accepted) | Valores permitidos |
| Bindable `Action` | Operation bound to an entity type: `POST /Orders(id)/Close` | Acción ligada a la entidad |

**UDF/UDT/UDO metadata**: since 9.1 PL05, user-defined fields, tables and objects appear in the metadata, so **metadata differs per company database**. Only UDTs of type *no object* are added (as simple single-table entities). This lets tools like WCF generate code for them.

> Note for this documentation set: the entity documentation in this folder was generated from a company `$metadata`; user-created UDFs/UDTs/UDOs were removed and only the SAP Argentina localization UDFs (`U_B1SYS_*`) were kept.

### 3.2.1 Metadata query with annotations (OData v4, FP 2608+)

From **SAP Business One 10.0 FP 2608**, `/b1s/v2/$metadata` accepts custom query options to retrieve only part of the metadata, enriched with labels and DB mappings. SAP warns the response format may change; **don't build SL extensions that depend on it**.

Annotation terms:

| Term | Applies to | Meaning | Significado (ES) |
|---|---|---|---|
| `Common.Label` | Entity set, property | Human-readable label (from the SAP Common vocabulary) | Etiqueta legible |
| `SAPB1.TableName` | Entity set | Internal DB table (e.g. `OCRD`) | Tabla de base de datos |
| `SAPB1.ColumnName` | Property | Internal DB column (e.g. `Phone1` → `Tel1`) | Columna de base de datos |
| `SAPB1.ValidValue` | Enum member | Stored DB value (e.g. `cCustomer` → `C`) | Valor almacenado en la BD |

Query options (custom SAP extensions, not OData standard):

| Option | Values | Effect | Efecto (ES) |
|---|---|---|---|
| `scope` | `entityset`, `enum` | Restrict output to entity sets or enums | Limitar a entity sets o enums |
| `entityset` | Entity set name | With `scope=entityset`, focus on one object; omitted → only the list of entity sets | Un objeto en particular |
| `dependency` | `true` / `false` (default) | Include dependent enum and complex types | Incluir tipos dependientes |
| `annotation` | `label`, `labelWithTable`, `labelWithField` (comma-separated combinations allowed) | Which annotations to add | Qué anotaciones incluir |

Only scalar and enum properties are annotated (not complex/collection properties).

Examples:

```http
GET /b1s/v2/$metadata?scope=entityset&annotation=label
GET /b1s/v2/$metadata?scope=entityset&annotation=labelWithTable
GET /b1s/v2/$metadata?scope=entityset&annotation=labelWithField&entityset=BusinessPartners
GET /b1s/v2/$metadata?scope=entityset&annotation=labelWithField,labelWithTable&entityset=BusinessPartners&dependency=true
```

Sample (abridged):

```xml
<EntitySet Name="BusinessPartners" EntityType="SAPB1.BusinessPartner">
  <Annotation Term="Common.Label" String="Business Partners"/>
  <Annotation Term="SAPB1.TableName" String="OCRD"/>
</EntitySet>
<Property Name="CardCode" Type="Edm.String">
  <Annotation Term="Common.Label" String="BP Code"/>
  <Annotation Term="SAPB1.ColumnName" String="CardCode"/>
</Property>
<Member Name="cCustomer" Value="0"><Annotation Term="SAPB1.ValidValue" String="C"/></Member>
```

Typical uses: object pickers (`label`), technical mapping (`labelWithTable`), field mapping in middleware (`labelWithField`), code generation/caching (`dependency=true`).

## 3.3 Service document

List of exposed entity sets:

```http
GET /
```

```json
{ "value": [ { "name": "ChartOfAccounts", "kind": "EntitySet", "url": "ChartOfAccounts" },
             { "name": "SalesStages", "kind": "EntitySet", "url": "SalesStages" }, ... ] }
```
