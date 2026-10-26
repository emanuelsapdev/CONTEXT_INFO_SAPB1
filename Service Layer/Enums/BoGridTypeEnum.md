# BoGridTypeEnum — Tipo de cuadrícula

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoGridTypeEnum`
- **Descripción (ES):** Tipo de cuadrícula
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `gtCombination` | 0 | Combination | Combinación |
| `gtContinuousLine` | 1 | Continuous Line | Línea continua |
| `gtBrokenLine` | 2 | Broken Line | Línea discontinua |
| `gtDots` | 3 | Dots | Puntos |

## Used by (1 properties)

- [ReportLayout](../Tipos-Complejos/ReportLayout.md).`GridType`
