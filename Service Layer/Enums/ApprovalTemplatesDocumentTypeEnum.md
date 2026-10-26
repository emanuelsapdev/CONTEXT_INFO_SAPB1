# ApprovalTemplatesDocumentTypeEnum — Tipo de documento del modelo de autorización

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ApprovalTemplatesDocumentTypeEnum`
- **Descripción (ES):** Tipo de documento del modelo de autorización
- **Underlying type:** Edm.Int32
- **Members:** 31

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `atdtQuotation` | 23 | Quotation | Oferta de ventas |
| `atdtOrder` | 17 | Order | Pedido de cliente |
| `atdtDelivery` | 15 | Delivery | Entrega |
| `atdtReturns` | 16 | Returns | Devolución |
| `atdtArDownPayment` | 203 | Ar Down Payment | Anticipo de clientes |
| `atdtArInvoice` | 13 | Ar Invoice | Factura de clientes |
| `atdtArCreditMemo` | 14 | Ar Credit Memo | Nota de crédito de clientes |
| `atdtCorrectionInvoice` | 132 | Correction Invoice | Factura de corrección |
| `atdtPurchaseOrder` | 22 | Purchase Order | Pedido de compra |
| `atdtGoodsReceiptPO` | 20 | Goods Receipt PO | Pedido de entrada de mercancías |
| `atdtGoodsReturns` | 21 | Goods Returns | Devolución de mercancías |
| `atdtApDownPayment` | 204 | Ap Down Payment | Anticipo de proveedores |
| `atdtApInvoice` | 18 | Ap Invoice | Factura de proveedores |
| `atdtApCreditMemo` | 19 | Ap Credit Memo | Nota de crédito de proveedores |
| `atdtGoodsReceipt` | 59 | Goods Receipt | Entrada de mercancías |
| `atdtGoodsIssue` | 60 | Goods Issue | Salida de mercancías |
| `atdtInventoryTransfer` | 67 | Inventory Transfer | Transferencia de stock |
| `atdtPurchaseQuotation` | 540000006 | Purchase Quotation | Oferta de compra |
| `atdtInventoryTransferRequest` | 1250000001 | Inventory Transfer Request | Solicitud de transferencia de stock |
| `atdtOutgoingPayment` | 46 | Outgoing Payment | Pago efectuado |
| `atdtInventoryCounting` | 1470000065 | Inventory Counting | Recuento de inventario |
| `atdtInventoryPosting` | 10000071 | Inventory Posting | Contabilización de inventario |
| `atdtInventoryOpeningBalance` | 310000001 | Inventory Opening Balance | Saldo inicial de inventario |
| `atdtReturnRequest` | 234000031 | Return Request | Solicitud de devolución |
| `atdtGoodsReturnRequest` | 234000032 | Goods Return Request | Solicitud de devolución de mercancías |
| `atdtBlanketAgreement` | 1250000025 | Blanket Agreement | Acuerdo global |
| `atdtSalesBlanketAgreement` | 1250000026 | Sales Blanket Agreement | Acuerdo global de ventas |
| `atdtPurchaseBlanketAgreement` | 1250000027 | Purchase Blanket Agreement | Acuerdo global de compras |
| `atdtPurchaseRequest` | 1470000113 | Purchase Request | Solicitud de compra |
| `atdtSelfInvoice` | 254000065 | Self Invoice | Autofactura |
| `atdtSelfCreditMemo` | 254000066 | Self Credit Memo | Autonota de crédito |

## Used by (1 properties)

- [ApprovalTemplateDocument](../Tipos-Complejos/ApprovalTemplateDocument.md).`DocumentType`
