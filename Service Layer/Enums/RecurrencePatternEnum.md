# RecurrencePatternEnum — Patrón de recurrencia

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `RecurrencePatternEnum`
- **Descripción (ES):** Patrón de recurrencia
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `rpNone` | 0 | None | Ninguno |
| `rpDaily` | 1 | Daily | Diario |
| `rpWeekly` | 2 | Weekly | Semanal |
| `rpMonthly` | 3 | Monthly | Mensual |
| `rpAnnually` | 4 | Annually | Anual |

## Used by (1 properties)

- [Activity](../Entidades/Activities.md).`RecurrencePattern`
