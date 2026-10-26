# BoRoundingMethod — Método de redondeo de precios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoRoundingMethod`
- **Descripción (ES):** Método de redondeo de precios
- **Underlying type:** Edm.Int32
- **Members:** 6

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `borm_FixedEnding` | 0 | Fixed Ending | Terminación fija |
| `borm_FixedInterval` | 1 | Fixed Interval | Intervalo fijo |
| `borm_NoRounding` | 2 | Number Rounding | Sin redondeo |
| `borm_RoundToFullAmount` | 3 | Round To Full Amount | Redondear a importe entero |
| `borm_RoundToFullDecAmount` | 4 | Round To Full Dec Amount | Redondear a décimas |
| `borm_RoundToFullTensAmount` | 5 | Round To Full Tens Amount | Redondear a decenas |

## Used by (2 properties)

- [BudgetScenario](../Entidades/BudgetScenarios.md).`RoundingMethod`
- [PriceList](../Entidades/PriceLists.md).`RoundingMethod`
