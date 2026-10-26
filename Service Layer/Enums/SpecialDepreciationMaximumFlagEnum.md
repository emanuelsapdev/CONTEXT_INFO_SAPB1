# SpecialDepreciationMaximumFlagEnum — Indicador de máximo de amortización especial

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `SpecialDepreciationMaximumFlagEnum`
- **Descripción (ES):** Indicador de máximo de amortización especial
- **Underlying type:** Edm.Int32
- **Members:** 2

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `spmfPercentage` | 0 | Percentage | Porcentaje |
| `spmfAmount` | 1 | Amount | Importe |

## Used by (1 properties)

- [DepreciationType](../Entidades/DepreciationTypes.md).`SpecialDepreciationMaximumFlag`
