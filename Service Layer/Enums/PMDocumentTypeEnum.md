# PMDocumentTypeEnum — Tipo de documento de gestión de proyectos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `PMDocumentTypeEnum`
- **Descripción (ES):** Tipo de documento de gestión de proyectos
- **Underlying type:** Edm.Int32
- **Members:** 30

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `pmdt_DocumentDraft` | 112 | Document Draft | Borrador de documento |
| `pmdt_ManualJournalEntry` | 30 | Manual Journal Entry | Asiento manual |
| `pmdt_SalesQuotation` | 23 | Sales Quotation | Oferta de ventas |
| `pmdt_SalesOrder` | 17 | Sales Order | Pedido de cliente |
| `pmdt_Delivery` | 15 | Delivery | Entrega |
| `pmdt_Return` | 16 | Return | Devolución |
| `pmdt_ReturnRequest` | 234000031 | Return Request | Solicitud de devolución |
| `pmdt_ARDownPaymentRequest` | 203002 | AR Down Payment Request | Solicitud de anticipo de clientes |
| `pmdt_ARDownPaymentInvoice` | 203 | AR Down Payment Invoice | Factura de anticipo de clientes |
| `pmdt_ARInvoice` | 13 | AR Invoice | Factura de clientes |
| `pmdt_ARCreditMemo` | 14 | AR Credit Memo | Nota de crédito de clientes |
| `pmdt_ARReserveInvoice` | 13002 | AR Reserve Invoice | Factura de reserva de clientes |
| `pmdt_PurchaseQuotation` | 540000006 | Purchase Quotation | Oferta de compra |
| `pmdt_PurchaseOrder` | 22 | Purchase Order | Pedido de compra |
| `pmdt_PurchaseRequest` | 1470000113 | Purchase Request | Solicitud de compra |
| `pmdt_GoodsReceiptPO` | 20 | Goods Receipt PO | Pedido de entrada de mercancías |
| `pmdt_GoodsReturn` | 21 | Goods Return | Devolución de mercancías |
| `pmdt_GoodsReturnRequest` | 234000032 | Goods Return Request | Solicitud de devolución de mercancías |
| `pmdt_APDownPaymentRequest` | 204002 | AP Down Payment Request | Solicitud de anticipo de proveedores |
| `pmdt_APDownPaymentInvoice` | 204 | AP Down Payment Invoice | Factura de anticipo de proveedores |
| `pmdt_APInvoice` | 18 | AP Invoice | Factura de proveedores |
| `pmdt_APCreditMemo` | 19 | AP Credit Memo | Nota de crédito de proveedores |
| `pmdt_APReserveInvoice` | 18002 | AP Reserve Invoice | Factura de reserva de proveedores |
| `pmdt_ServiceCall` | 191 | Service Call | Llamada de servicio |
| `pmdt_GoodsReceipt` | 59 | Goods Receipt | Entrada de mercancías |
| `pmdt_GoodsIssue` | 60 | Goods Issue | Salida de mercancías |
| `pmdt_ARCorrectionInvoice` | 165 | AR Correction Invoice | Factura de corrección de clientes |
| `pmdt_ARCorrectionInvoiceReversal` | 166 | AR Correction Invoice Reversal | Anulación de factura de corrección de clientes |
| `pmdt_APCorrectionInvoice` | 163 | AP Correction Invoice | Factura de corrección de proveedores |
| `pmdt_APCorrectionInvoiceReversal` | 164 | AP Correction Invoice Reversal | Anulación de factura de corrección de proveedores |

## Used by (2 properties)

- [PMS_DocumentData](../Tipos-Complejos/PMS_DocumentData.md).`DocType`
- [PM_DocumentData](../Tipos-Complejos/PM_DocumentData.md).`DocType`
