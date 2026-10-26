# ResourceDailyCapacity — Capacidad diaria del recurso

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ResourceDailyCapacity`
- **Descripción (ES):** Capacidad diaria del recurso
- **Description (EN):** Resource Daily Capacity

- **Properties:** 9

## Properties (9)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` | Edm.String | Yes | Code | Código |
| 2 | `Weekday` | [ResourceDailyCapacityWeekdayEnum](../Enums/ResourceDailyCapacityWeekdayEnum.md) | Yes | Weekday | Día de la semana |
| 3 | `Factor1` | Edm.Double | Yes | Factor 1 | Factor 1 |
| 4 | `Factor2` | Edm.Double | Yes | Factor 2 | Factor 2 |
| 5 | `Factor3` | Edm.Double | Yes | Factor 3 | Factor 3 |
| 6 | `Factor4` | Edm.Double | Yes | Factor 4 | Factor 4 |
| 7 | `Total` | Edm.Double | Yes | Total | Total |
| 8 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 9 | `SingleRun` | Edm.Double | Yes | Single Run | Ejecución única |

## Used by (properties)

- [Resource](../Entidades/Resources.md).`ResourceDailyCapacities`
