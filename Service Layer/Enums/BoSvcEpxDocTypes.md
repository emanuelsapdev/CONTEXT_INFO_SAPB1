# BoSvcEpxDocTypes — Tipo de documento de gastos de servicio

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoSvcEpxDocTypes`
- **Descripción (ES):** Tipo de documento de gastos de servicio
- **Underlying type:** Edm.Int32
- **Members:** 17

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `edt_Invoice` | 13 | Invoice | Factura de clientes |
| `edt_Delivery` | 15 | Delivery | Entrega |
| `edt_Return` | 16 | Return | Devolución |
| `edt_StockTransfer` | 67 | Stock Transfer | Transferencia de stock |
| `edt_CreditMemo` | 14 | Credit Memo | Nota de crédito de clientes |
| `edt_Order` | 17 | Order | Pedido de cliente |
| `edt_Quotation` | 23 | Quotation | Oferta de ventas |
| `edt_AP_Invoice` | 18 | AP Invoice | Factura de proveedores |
| `edt_AP_CreditMemo` | 19 | AP Credit Memo | Nota de crédito de proveedores |
| `edt_GoodsReceipt` | 20 | Goods Receipt | Pedido de entrada de mercancías |
| `edt_GoodsReturn` | 21 | Goods Return | Devolución de mercancías |
| `edt_PurchaseOrder` | 22 | Purchase Order | Pedido de compra |
| `edt_PurchaseQuotation` | 540000006 | Purchase Quotation | Oferta de compra |
| `edt_AR_CorrectionInvoice` | 165 | AR Correction Invoice | Factura de corrección de clientes |
| `edt_AP_CorrectionInvoice` | 163 | AP Correction Invoice | Factura de corrección de proveedores |
| `edt_Return_Request` | 234000031 | Return Request | Solicitud de devolución |
| `edt_Goods_Return_Request` | 234000032 | Goods Return Request | Solicitud de devolución de mercancías |

## Used by (1 properties)

- [ServiceCallInventoryExpense](../Tipos-Complejos/ServiceCallInventoryExpense.md).`DocumentType`
