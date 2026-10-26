# RoundingSysEnum — Sistema de redondeo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `RoundingSysEnum`
- **Descripción (ES):** Sistema de redondeo
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `rsNoRounding` | 0 | Number Rounding | Sin redondeo |
| `rsRoundToFiveHundredth` | 1 | Round To Five Hundredth | Redondear a 0,05 |
| `rsRoundToOne` | 2 | Round To One | Redondear a 1 |
| `rsRoundToTen` | 3 | Round To Ten | Redondear a 10 |
| `rsRoundToTenHundredth` | 4 | Round To Ten Hundredth | Redondear a 0,10 |

## Used by (1 properties)

- [Currency](../Entidades/Currencies.md).`Rounding`
