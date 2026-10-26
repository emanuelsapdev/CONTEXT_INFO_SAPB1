# BoCurrencySources — Origen de la moneda

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoCurrencySources`
- **Descripción (ES):** Origen de la moneda
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `bocs_LocalCurrency` | 0 | Local Currency | Moneda local |
| `bocs_SystemCurrency` | 1 | System Currency | Moneda del sistema |
| `bocs_BPCurrency` | 2 | Business Partner Currency | Moneda del socio de negocios |

## Used by (2 properties)

- [PurchaseTaxInvoice](../Entidades/PurchaseTaxInvoices.md).`CurrencySource`
- [SalesTaxInvoice](../Entidades/SalesTaxInvoices.md).`CurrencySource`
