# BoWeekEnum — Día de la semana

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoWeekEnum`
- **Descripción (ES):** Día de la semana
- **Underlying type:** Edm.Int32
- **Members:** 7

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `Sunday` | 1 | Sunday | Domingo |
| `Monday` | 2 | Monday | Lunes |
| `Tuesday` | 3 | Tuesday | Martes |
| `Wednesday` | 4 | Wednesday | Miércoles |
| `Thursday` | 5 | Thursday | Jueves |
| `Friday` | 6 | Friday | Viernes |
| `Saturday` | 7 | Saturday | Sábado |

## Used by (2 properties)

- [Holiday](../Entidades/Holidays.md).`WeekendFrom`
- [Holiday](../Entidades/Holidays.md).`WeekendTO`
