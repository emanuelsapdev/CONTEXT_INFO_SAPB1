# GSTTransactionTypeEnum — Tipo de transacción GST

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `GSTTransactionTypeEnum`
- **Descripción (ES):** Tipo de transacción GST
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `gsttrantyp_BillOfSupply` | 0 | Bill Of Supply | Factura de suministro |
| `gsttrantyp_GSTTaxInvoice` | 1 | GST Tax Invoice | Factura de impuestos GST |
| `gsttrantyp_GSTDebitMemo` | 2 | GST Debit Memo | Nota de débito GST |

## Used by (1 properties)

- [Document](../Entidades/PurchaseQuotations.md).`GSTTransactionType`
