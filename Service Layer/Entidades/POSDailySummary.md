# POSDailySummary — Resumen diario de POS

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `POSDailySummary`
- **Descripción (ES):** Resumen diario de POS
- **Entity type:** `POSDailySummary`
- **Key:** `AbsEntry` (Edm.Int32)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 11 · **Navigation properties:** 27 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/POSDailySummary?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/POSDailySummary/$count` | Contar |
| Get by key | `GET /b1s/v2/POSDailySummary(1)` | Obtener por clave |
| Create | `POST /b1s/v2/POSDailySummary` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/POSDailySummary(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/POSDailySummary(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/POSDailySummary(1)` (only if the B1 object allows removal) | Borrar |

## Properties (11)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` 🔑 | Edm.Int32 | No | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `Date` | Edm.DateTimeOffset | Yes | Date | Fecha |
| 3 | `EquipmentNo` | Edm.String | Yes | Equipment Number | Número de equipo |
| 4 | `CounterPosition` | Edm.Int32 | Yes | Counter Position | Posición del contador |
| 5 | `ResetCounterPosition` | Edm.Int32 | Yes | Reset Counter Position | Restablecer posición del contador |
| 6 | `OperationCounter` | Edm.Int32 | Yes | Operation Counter | Contador de operaciones |
| 7 | `Total` | Edm.Double | Yes | Total | Total |
| 8 | `GrossSales` | Edm.Double | Yes | Gross Sales | Ventas brutas |
| 9 | `PISTotal` | Edm.Double | Yes | PIS Total | Total de PIS |
| 10 | `COFINSTotal` | Edm.Double | Yes | COFINS Total | Total de COFINS |
| 11 | `POSTotalizerCollection` | Collection([POSTotalizer](../Tipos-Complejos/POSTotalizer.md)) | Yes | POS Totalizer Collection | Colección de totalizadores POS |

## Navigation properties (27)

Use `GET /b1s/v2/POSDailySummary(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `PurchaseQuotations` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseQuotations](PurchaseQuotations.md) |  | Ofertas de compra |
| `CorrectionInvoiceReversal` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionInvoiceReversal](CorrectionInvoiceReversal.md) |  | Anulación de factura de corrección de clientes |
| `CorrectionInvoice` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionInvoice](CorrectionInvoice.md) |  | Factura de corrección de clientes |
| `PurchaseDeliveryNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseDeliveryNotes](PurchaseDeliveryNotes.md) |  | Pedidos de entrada de mercancías |
| `CorrectionPurchaseInvoice` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionPurchaseInvoice](CorrectionPurchaseInvoice.md) |  | Factura de corrección de proveedores |
| `InventoryGenEntries` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [InventoryGenEntries](InventoryGenEntries.md) |  | Entradas de mercancías |
| `Orders` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Orders](Orders.md) |  | Pedidos de cliente (órdenes de venta) |
| `InventoryGenExits` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [InventoryGenExits](InventoryGenExits.md) |  | Salidas de mercancías |
| `Drafts` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Drafts](Drafts.md) |  | Borradores de documentos |
| `ReturnRequest` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [ReturnRequest](ReturnRequest.md) |  | Solicitudes de devolución de clientes |
| `DeliveryNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [DeliveryNotes](DeliveryNotes.md) |  | Entregas |
| `PurchaseInvoices` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseInvoices](PurchaseInvoices.md) |  | Facturas de proveedores |
| `SelfInvoices` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [SelfInvoices](SelfInvoices.md) |  | Autofacturas |
| `Invoices` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Invoices](Invoices.md) |  | Facturas de clientes |
| `CreditNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CreditNotes](CreditNotes.md) |  | Notas de crédito de clientes |
| `PurchaseCreditNotes` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseCreditNotes](PurchaseCreditNotes.md) |  | Notas de crédito de proveedores |
| `DownPayments` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [DownPayments](DownPayments.md) |  | Facturas de anticipo de clientes |
| `PurchaseDownPayments` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseDownPayments](PurchaseDownPayments.md) |  | Facturas de anticipo de proveedores |
| `PurchaseReturns` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseReturns](PurchaseReturns.md) |  | Devoluciones de mercancías a proveedores |
| `PurchaseOrders` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseOrders](PurchaseOrders.md) |  | Pedidos de compra (órdenes de compra) |
| `SelfCreditMemos` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [SelfCreditMemos](SelfCreditMemos.md) |  | Autonotas de crédito |
| `Quotations` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Quotations](Quotations.md) |  | Ofertas de ventas (cotizaciones) |
| `Returns` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [Returns](Returns.md) |  | Devoluciones de clientes |
| `FiscalPrinter` | [FiscalPrinter](../Entidades/FiscalPrinter.md) | [FiscalPrinter](FiscalPrinter.md) | EquipmentNo → EquipmentNo | Impresora fiscal |
| `GoodsReturnRequest` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [GoodsReturnRequest](GoodsReturnRequest.md) |  | Solicitudes de devolución de mercancías |
| `CorrectionPurchaseInvoiceReversal` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [CorrectionPurchaseInvoiceReversal](CorrectionPurchaseInvoiceReversal.md) |  | Anulación de factura de corrección de proveedores |
| `PurchaseRequests` | Collection([Document](../Entidades/PurchaseQuotations.md)) | [PurchaseRequests](PurchaseRequests.md) |  | Solicitudes de compra |
