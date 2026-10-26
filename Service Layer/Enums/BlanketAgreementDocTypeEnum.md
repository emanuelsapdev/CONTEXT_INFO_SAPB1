# BlanketAgreementDocTypeEnum — Tipo de documento del acuerdo global

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BlanketAgreementDocTypeEnum`
- **Descripción (ES):** Tipo de documento del acuerdo global
- **Underlying type:** Edm.Int32
- **Members:** 18

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `ARInvoice` | 0 | AR Invoice | Factura de clientes |
| `ARCreditMemo` | 1 | AR Credit Memo | Nota de crédito de clientes |
| `Delivery` | 2 | Delivery | Entrega |
| `Return` | 3 | Return | Devolución |
| `SalesOrder` | 4 | Sales Order | Pedido de cliente |
| `APInvoice` | 5 | AP Invoice | Factura de proveedores |
| `APCreditMemo` | 6 | AP Credit Memo | Nota de crédito de proveedores |
| `GoodsReceiptPO` | 7 | Goods Receipt PO | Pedido de entrada de mercancías |
| `GoodsReturn` | 8 | Goods Return | Devolución de mercancías |
| `PurchaseOrder` | 9 | Purchase Order | Pedido de compra |
| `SalesQuotation` | 10 | Sales Quotation | Oferta de ventas |
| `APCorrectionInvoice` | 11 | AP Correction Invoice | Factura de corrección de proveedores |
| `APCorrectionInvoiceReversal` | 12 | AP Correction Invoice Reversal | Anulación de factura de corrección de proveedores |
| `ARCorrectionInvoice` | 13 | AR Correction Invoice | Factura de corrección de clientes |
| `ARCorrectionInvoiceReversal` | 14 | AR Correction Invoice Reversal | Anulación de factura de corrección de clientes |
| `ARDownPayment` | 15 | AR Down Payment | Anticipo de clientes |
| `APDownPayment` | 16 | AP Down Payment | Anticipo de proveedores |
| `PurchaseQuotation` | 17 | Purchase Quotation | Oferta de compra |

## Used by (1 properties)

- [BlanketAgreementsDocument](../Tipos-Complejos/BlanketAgreementsDocument.md).`DocumentType`
