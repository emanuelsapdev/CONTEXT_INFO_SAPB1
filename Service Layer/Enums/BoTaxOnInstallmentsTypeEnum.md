# BoTaxOnInstallmentsTypeEnum — Impuesto sobre cuotas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoTaxOnInstallmentsTypeEnum`
- **Descripción (ES):** Impuesto sobre cuotas
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `toiProportionally` | 0 | Proportionally | Proporcional |
| `toiTaxInFirst` | 1 | Tax In First | Impuesto en la primera cuota |
| `toiTaxInFirstOnly` | 2 | Tax In First Only | Impuesto solo en la primera cuota |

## Used by (1 properties)

- [Document](../Entidades/PurchaseQuotations.md).`TaxOnInstallments`
