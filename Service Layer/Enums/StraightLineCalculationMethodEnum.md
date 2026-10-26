# StraightLineCalculationMethodEnum — Método de cálculo lineal

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `StraightLineCalculationMethodEnum`
- **Descripción (ES):** Método de cálculo lineal
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `slcmAuquisitionValueDividedByTotalUsefulLife` | 0 | Auquisition Value Divided By Total Useful Life | Valor de adquisición / vida útil total |
| `slcmPercentageOfAcquisitionValue` | 1 | Percentage Of Acquisition Value | Porcentaje del valor de adquisición |
| `slcmNetBookValueDividedByRemainingLife` | 2 | Net Book Value Divided By Remaining Life | Valor neto contable / vida restante |

## Used by (1 properties)

- [DepreciationType](../Entidades/DepreciationTypes.md).`StraightLineCalculationMethod`
