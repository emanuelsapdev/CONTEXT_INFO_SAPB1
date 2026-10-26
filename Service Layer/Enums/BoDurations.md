# BoDurations — Unidad de duración

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoDurations`
- **Descripción (ES):** Unidad de duración
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `du_Seconds` | -1 | Seconds | Segundos |
| `du_Minuts` | 0 | Minuts | Minutos |
| `du_Hours` | 1 | Hours | Horas |
| `du_Days` | 2 | Days | Días |

## Used by (9 properties)

- [Activity](../Entidades/Activities.md).`DurationType`
- [Activity](../Entidades/Activities.md).`ReminderType`
- [Contact](../Entidades/Contacts.md).`DurationType`
- [Contact](../Entidades/Contacts.md).`ReminderType`
- [ServiceCall](../Entidades/ServiceCalls.md).`DurationType`
- [ServiceCall](../Entidades/ServiceCalls.md).`ReminderType`
- [ServiceCallScheduling](../Tipos-Complejos/ServiceCallScheduling.md).`ActualDurationType`
- [ServiceCallScheduling](../Tipos-Complejos/ServiceCallScheduling.md).`DurationType`
- [ServiceCallScheduling](../Tipos-Complejos/ServiceCallScheduling.md).`ReminderType`
