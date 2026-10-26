# 3.10–3.12 Individual Properties, Associations (Navigation) and User-Defined Schemas

> Source: *Working with SAP Business One Service Layer* v1.29, sections 3.10–3.12 (paraphrased technical reference).
>
> **Resumen (ES):** leer una sola propiedad (y su valor crudo), navegar entre entidades relacionadas (`/Orders(1)/BusinessPartner`, `$expand`) y limitar los campos devueltos con esquemas definidos por el usuario (`B1S-Schema`).

## 3.10 Retrieving individual properties (9.1 PL04+)

| Request | Response | Petición (ES) |
|---|---|---|
| `GET /Orders(1)/DocEntry` (exists) | `200 OK` `{"value": 1}` | Valor de una propiedad |
| `GET /Orders(1)/DocEntry` (null / not found) | `200 OK` `{"odata.null": true}` (`"@odata.null"` in OData v4) | Valor nulo |
| `GET /Orders(1)/DocEntry/$value` | `200 OK` body `1` (raw value) | Valor crudo |
| `$value` on a null | `404 Not Found`, code `-2028`, "Resource not found for the property: DocEntry" | Valor crudo nulo |

Not supported: properties of a **complex type**, e.g. `GET /Orders(1)/TaxExtension/TaxId0`.

## 3.11 Associations and navigation properties (9.1 PL05+)

Entities can be related through navigation properties defined in the metadata. Example: `GET Orders(1)/BusinessPartner` returns the order's customer — the same as `GET BusinessPartners('c1')` if the order's `CardCode` is `c1`. You can keep navigating: `GET Orders(1)/BusinessPartner/ForeignName` ≡ `GET BusinessPartners('c1')/ForeignName`.

### Metadata definitions (OData v3 example)

| Section | Meaning | Significado (ES) |
|---|---|---|
| `Association FK_Documents_BusinessPartners` | 1:n relation BusinessPartner (0..1) ↔ Document (*), joined on `CardCode` (principal `BusinessPartners.CardCode`, dependent `Documents.CardCode`) | Relación 1:n por CardCode |
| `NavigationProperty Orders`, `Invoices` on `BusinessPartner` | From a BP to its documents | Desde el SN a sus documentos |
| `NavigationProperty BusinessPartner` on `Document` | From a document to its BP | Desde el documento a su SN |
| `AssociationSet FK_Orders_BusinessPartners`, `FK_Invoices_BusinessPartners` | Bind the association to concrete entity sets | Vincula la relación a los entity sets |

In OData v4 (`/b1s/v2`) the equivalent is `NavigationProperty` + `ReferentialConstraint` on the entity type and `NavigationPropertyBinding` on the entity set (see the *Entidades* docs in this folder, section "Navigation properties").

### 3.11.2 Navigating as an entity

Navigation can be one-way or two-way.

| Request | Equivalent | Petición (ES) |
|---|---|---|
| `GET BusinessPartners('c1')/Orders` | `GET Orders?$filter=CardCode eq 'c1'` | Pedidos de un SN |
| `GET Orders(1)/BusinessPartner` | `GET BusinessPartners('<CardCode of order 1>')` | SN de un pedido |
| `GET Orders(1)/BusinessPartner/Orders` | All orders of the customer of order 1 | Cadena de navegación |

### 3.11.3 Navigating with `$expand`

| Request | Effect | Efecto (ES) |
|---|---|---|
| `GET Orders(1)?$select=*,BusinessPartner&$expand=BusinessPartner` | Order + embedded customer | Pedido con su cliente embebido |
| `GET Orders(1)?$select=CardCode,BusinessPartner/ForeignName&$expand=BusinessPartner` | Order CardCode + customer ForeignName | Campos de ambos |
| `GET Orders?$select=*,BusinessPartner&$expand=BusinessPartner` | For every order | Para toda la colección |

Notes:
- `GET Orders(1)?$select=CardCode,BusinessPartner/ForeignName` **without** `$expand` ignores `BusinessPartner/ForeignName`.
- `$expand` on collections can be slow → don't call it frequently.
- Since FP 2105 you can nest `$select` inside `$expand` — see [03-03 Query Options](03-03-Query-Options.md#3611-expand-enhancements-fp-2105).

## 3.12 User-defined schemas (9.1 PL03+)

Restrict the fields returned for entity/complex types with a JSON **schema file**.

Prerequisites:

| Item | Detail | Detalle (ES) |
|---|---|---|
| Location | `<Installation Directory>/ServiceLayer/conf/` | Carpeta `conf` |
| Multi-node | If you call a load balancer member on another machine directly, copy the schema file there too | Copiar a cada nodo |
| Reload | Changes apply immediately on save (no restart) | Sin reinicio |
| Default schema | Name the file like the `Schema` option in `b1s.conf` to apply it without the header (see [06 Configuration](06-Configuration-and-Logs.md)) | Esquema por defecto |
| File name | Any name (`*.schema` is conventional). `demo.schema` ships with SL since 9.1 PL04 | Cualquier nombre |

Example `conf/marketingDocument.schema`:

```json
{
  "Document":     [ "DocEntry", "DocNum", "DocumentLines" ],
  "DocumentLine": [ "LineNum", "ItemCode", "Quantity" ]
}
```

- Keys are **type names** (EntityType or ComplexType). `Document` applies to **all marketing documents** (Orders, Invoices, …).
- Use it per request with header **`B1S-Schema: <file name>`**; the response echoes the header.

```http
GET /Orders
B1S-Schema: demo.schema
```

```json
HTTP/1.1 200 OK
B1S-Schema: schema1.schema
{ "DocEntry": 71, "DocNum": 51,
  "DocumentLines": [ { "LineNum": 0, "ItemCode": "i1", "Quantity": 10 }, { "LineNum": 1, "ItemCode": "i2", "Quantity": 8 } ] }
```

For UDOs, schema keys use the **UDO/sub-object name**, not the code (see [03-08](03-08-UDF-UDT-UDO.md)).
