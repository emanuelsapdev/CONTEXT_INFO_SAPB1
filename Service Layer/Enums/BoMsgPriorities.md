# BoMsgPriorities — Prioridad del mensaje

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoMsgPriorities`
- **Descripción (ES):** Prioridad del mensaje
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `pr_Low` | 0 | Low | Baja |
| `pr_Normal` | 1 | Normal | Normal |
| `pr_High` | 2 | High | Alta |

## Used by (4 properties)

- [Activity](../Entidades/Activities.md).`Priority`
- [ActivityParams](../Tipos-Complejos/ActivityParams.md).`Priority`
- [Contact](../Entidades/Contacts.md).`Priority`
- [Message](../Entidades/Messages.md).`Priority`
