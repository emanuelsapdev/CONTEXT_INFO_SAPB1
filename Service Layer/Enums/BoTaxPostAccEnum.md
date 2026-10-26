# BoTaxPostAccEnum — Cuenta de contabilización de impuestos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoTaxPostAccEnum`
- **Descripción (ES):** Cuenta de contabilización de impuestos
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `tpa_Default` | 0 | Default | Predeterminada |
| `tpa_SalesTaxAccount` | 1 | Sales Tax Account | Cuenta de impuesto de ventas |
| `tpa_PurchaseTaxAccount` | 2 | Purchase Tax Account | Cuenta de impuesto de compras |

## Used by (1 properties)

- [JournalEntryLine](../Tipos-Complejos/JournalEntryLine.md).`TaxPostAccount`
