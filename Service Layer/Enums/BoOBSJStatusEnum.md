# BoOBSJStatusEnum — Estado del trabajo en segundo plano

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoOBSJStatusEnum`
- **Descripción (ES):** Estado del trabajo en segundo plano
- **Underlying type:** Edm.Int32
- **Members:** 7

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `bobsjScheduled` | 0 | Scheduled | Programado |
| `bobsjRunning` | 1 | Running | En ejecución |
| `bobsjError` | 2 | Error | Error |
| `bobsjFinished` | 3 | Finished | Finalizado |
| `bobsjPending` | 4 | Pending | Pendiente |
| `bobsjCreating` | 5 | Creating | Creando |
| `bobsjCancel` | 6 | Cancel | Cancelado |

## Used by (2 properties)

- [ScheduleJob](../Entidades/ScheduleJobService.md).`Status`
- [ScheduleJobParams](../Tipos-Complejos/ScheduleJobParams.md).`Status`
