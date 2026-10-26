# RecurrenceDayOfWeekEnum — Día de la semana de la recurrencia

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `RecurrenceDayOfWeekEnum`
- **Descripción (ES):** Día de la semana de la recurrencia
- **Underlying type:** Edm.Int32
- **Members:** 10

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `rdowDay` | 0 | Day | Día |
| `rdowWeekDay` | 1 | Week Day | Día laborable |
| `rdowWeekendDay` | 2 | Weekend Day | Día de fin de semana |
| `rdowSun` | 3 | Sun | Domingo |
| `rdowMon` | 4 | Mon | Lunes |
| `rdowTue` | 5 | Tue | Martes |
| `rdowWed` | 6 | Wed | Miércoles |
| `rdowThu` | 7 | Thu | Jueves |
| `rdowFri` | 8 | Fri | Viernes |
| `rdowSat` | 9 | Sat | Sábado |

## Used by (2 properties)

- [Activity](../Entidades/Activities.md).`RecurrenceDayOfWeek`
- [InventoryCycles](../Entidades/InventoryCycles.md).`RecurrenceDayOfWeek`
