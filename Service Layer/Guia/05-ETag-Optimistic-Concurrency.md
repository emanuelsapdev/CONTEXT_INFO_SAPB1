# 5. Service Layer ETag (optimistic concurrency)

> Source: *Working with SAP Business One Service Layer* v1.29, chapter 5 (paraphrased technical reference).
>
> **Resumen (ES):** usar ETag e `If-Match` para evitar sobrescribir cambios de otro usuario al actualizar, borrar o ejecutar acciones; qué entidades lo soportan y cómo se ve en el metadata.

## 5.1 Concept

- **Optimistic concurrency**: no locks; instead each read returns a version token and writes are rejected if the resource changed meanwhile. Suited to systems with rare conflicts and high throughput.
- HTTP mechanism: the response includes an **ETag**; subsequent writes send it in **`If-Match`**; an out-of-date ETag → rejected.
- SL uses **weak ETags**: `ETag: W/"<hashed string>"` (semantic equivalence).
- Available since **SAP Business One 10.0 FP 2102**, OData-compliant.

## 5.2 Scenarios

| Scenario | Request | Result | Escenario (ES) |
|---|---|---|---|
| Create | `POST /b1s/v2/Items` `{"ItemCode": "i002"}` | `201`, header `ETag: W/"356A19..."` and body `"@odata.etag": "W/\"356A19...\""` | Al crear se devuelve el ETag |
| Read | `GET /b1s/v2/Items('i002')` | `200` with `ETag` header and `@odata.etag` | Al leer se devuelve el ETag |
| Update | `PATCH /b1s/v2/Items('i002')` + `If-Match: W/"356A19..."` `{"ItemName": "name2"}` | Unchanged → `204`; changed by someone else → **`412 Precondition Failed`** | Actualizar solo si no cambió |
| Delete | `DELETE /b1s/v2/Items('i002')` + `If-Match: W/"..."` | Changed meanwhile → `412` | Borrar solo una versión concreta |
| Bound action | `POST /b1s/v2/Orders(8)/Cancel` + `If-Match: W/"..."` | Changed meanwhile → `412` | Acción solo sobre una versión concreta |

Without `If-Match`, PATCH/DELETE/actions apply regardless of concurrent changes (DELETE returns `404` only if the entity doesn't exist).

`412` body:

```json
{ "error": { "code": "-2039",
  "message": "Another user or another operation modified data; to continue, open the window again (ODBC -2039)" } }
```

## 5.3 Entities with ETag (FP 2102)

| Entity sets | Grupo (ES) |
|---|---|
| Quotations, Orders, DeliveryNotes, Returns, ReturnRequest, DownPayments, Invoices, CreditNotes, CorrectionInvoice, CorrectionInvoiceReversal | Ventas |
| PurchaseRequests, PurchaseQuotations, PurchaseOrders, PurchaseDeliveryNotes, GoodsReturnRequest, PurchaseReturns, PurchaseDownPayments, PurchaseInvoices, PurchaseCreditNotes, CorrectionPurchaseInvoice, CorrectionPurchaseInvoiceReversal | Compras |
| Drafts, InventoryGenEntries, InventoryGenExits | Borradores e inventario |
| Activities, AdditionalExpenses, Items, BusinessPartners | Otros |

(The metadata used for this documentation set marks more entity sets with `OptimisticConcurrency` — e.g. `SQLQueries`; check each entity's doc page, section *ETag*.)

## 5.4 Metadata

OData v4 — annotation on the entity set:

```xml
<EntitySet EntityType="SAPB1.BusinessPartner" Name="BusinessPartners">
  <Annotation Term="Org.OData.Core.V1.OptimisticConcurrency">
    <Collection><PropertyPath>DataVersion</PropertyPath></Collection>
  </Annotation>
</EntitySet>
```

OData v3 — property attribute:

```xml
<Property ConcurrencyMode="Fixed" Name="DataVersion" Type="Edm.Int32"/>
```

The property used is **`DataVersion`**. SAP strongly recommends consuming SL with **OData v4** (`/b1s/v2`).
