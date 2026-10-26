# BoAPARDocumentTypes — Tipos de documentos de compras/ventas (ObjType)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoAPARDocumentTypes`
- **Descripción (ES):** Tipos de documentos de compras/ventas (ObjType)
- **Underlying type:** Edm.Int32
- **Members:** 16

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `bodt_Invoice` | 13 | Invoice | Factura de clientes (13) |
| `bodt_CreditNote` | 14 | Credit Note | Nota de crédito de clientes (14) |
| `bodt_DeliveryNote` | 15 | Delivery Note | Entrega (15) |
| `bodt_Return` | 16 | Return | Devolución (16) |
| `bodt_Order` | 17 | Order | Pedido de cliente (17) |
| `bodt_PurchaseInvoice` | 18 | Purchase Invoice | Factura de proveedores (18) |
| `bodt_PurchaseCreditNote` | 19 | Purchase Credit Note | Nota de crédito de proveedores (19) |
| `bodt_PurchaseDeliveryNote` | 20 | Purchase Delivery Note | Pedido de entrada de mercancías (20) |
| `bodt_PurchaseReturn` | 21 | Purchase Return | Devolución de mercancías (21) |
| `bodt_PurchaseOrder` | 22 | Purchase Order | Pedido de compra (22) |
| `bodt_Quotation` | 23 | Quotation | Oferta de ventas (23) |
| `bodt_CorrectionAPInvoice` | 163 | Correction AP Invoice | Factura de corrección de proveedores |
| `bodt_CorrectionARInvoice` | 165 | Correction AR Invoice | Factura de corrección de clientes |
| `bodt_Zero` | 166 | Zero | Cero |
| `bodt_MinusOne` | 167 | Minus One | Menos uno |
| `bodt_PurchaseQutation` | 540000006 | Purchase Qutation | Oferta de compra |

## Used by (2 properties)

- [LegalData](../Entidades/LegalData.md).`SourceObjectType`
- [SalesOpportunitiesLine](../Tipos-Complejos/SalesOpportunitiesLine.md).`DocumentType`
