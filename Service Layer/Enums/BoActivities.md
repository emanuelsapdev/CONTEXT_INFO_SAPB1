# BoActivities — Tipo de actividad

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoActivities`
- **Descripción (ES):** Tipo de actividad
- **Underlying type:** Edm.Int32
- **Members:** 6

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `cn_Conversation` | 0 | Conversation | Llamada telefónica |
| `cn_Meeting` | 1 | Meeting | Reunión |
| `cn_Task` | 2 | Task | Tarea |
| `cn_Other` | 3 | Other | Otra |
| `cn_Note` | 4 | Note | Nota |
| `cn_Campaign` | 5 | Campaign | Campaña |

## Used by (3 properties)

- [Activity](../Entidades/Activities.md).`ActivityProperty`
- [ActivityParams](../Tipos-Complejos/ActivityParams.md).`Activity`
- [Contact](../Entidades/Contacts.md).`Activity`
