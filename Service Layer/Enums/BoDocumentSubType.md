# BoDocumentSubType — Subtipo de documento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoDocumentSubType`
- **Descripción (ES):** Subtipo de documento
- **Underlying type:** Edm.Int32
- **Members:** 10

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `bod_None` | 0 | None | Ninguno |
| `bod_InvoiceExempt` | 1 | Invoice Exempt | Factura exenta |
| `bod_DebitMemo` | 2 | Debit Memo | Nota de débito |
| `bod_Bill` | 3 | Bill | Boleta |
| `bod_ExemptBill` | 4 | Exempt Bill | Boleta exenta |
| `bod_PurchaseDebitMemo` | 5 | Purchase Debit Memo | Nota de débito de compras |
| `bod_ExportInvoice` | 6 | Export Invoice | Factura de exportación |
| `bod_GSTTaxInvoice` | 7 | GST Tax Invoice | Factura de impuestos GST |
| `bod_GSTDebitMemo` | 8 | GST Debit Memo | Nota de débito GST |
| `bod_RefundVoucher` | 9 | Refund Voucher | Comprobante de reembolso |

## Used by (1 properties)

- [Document](../Entidades/PurchaseQuotations.md).`DocumentSubType`
