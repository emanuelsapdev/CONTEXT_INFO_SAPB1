# RoundingTypeEnum — Tipo de redondeo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `RoundingTypeEnum`
- **Descripción (ES):** Tipo de redondeo
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `rt_TruncatedAU` | 0 | Truncated AU | Truncado |
| `rt_CommercialValues` | 1 | Commercial Values | Valores comerciales |
| `rt_NoRounding` | 2 | Number Rounding | Sin redondeo |

## Used by (1 properties)

- [WithholdingTaxCode](../Entidades/WithholdingTaxCodes.md).`RoundingType`
