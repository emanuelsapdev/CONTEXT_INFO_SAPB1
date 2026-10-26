# ScheduleJobService — Trabajos programados

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ScheduleJobService`
- **Descripción (ES):** Trabajos programados
- **Entity type:** `ScheduleJob` (open type: accepts dynamic/UDF properties)
- **Key:** `JobID` (Edm.Int32)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 15 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ScheduleJobService?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ScheduleJobService/$count` | Contar |
| Get by key | `GET /b1s/v2/ScheduleJobService(1)` | Obtener por clave |
| Create | `POST /b1s/v2/ScheduleJobService` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ScheduleJobService(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ScheduleJobService(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/ScheduleJobService(1)` (only if the B1 object allows removal) | Borrar |

## Properties (15)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `JobID` 🔑 | Edm.Int32 | No | Job ID | ID de trabajo |
| 2 | `JobType` | Edm.String | Yes | Job Type | Tipo de trabajo |
| 3 | `Description` | Edm.String | Yes | Description | Descripción |
| 4 | `Status` | [BoOBSJStatusEnum](../Enums/BoOBSJStatusEnum.md) | Yes | Status | Estado |
| 5 | `ScheduleType` | [BoOBSJScheduleEnum](../Enums/BoOBSJScheduleEnum.md) | Yes | Schedule Type | Tipo de programación |
| 6 | `NextRunningDate` | Edm.DateTimeOffset | Yes | Next Running Date | Fecha de la siguiente ejecución |
| 7 | `NextRunningTime` | Edm.TimeOfDay | Yes | Next Running Time | Hora de la siguiente ejecución |
| 8 | `BeginFunctionParameters` | Edm.String | Yes | Begin Function Parameters | Parámetros de la función inicial |
| 9 | `EndFunctionParameters` | Edm.String | Yes | End Function Parameters | Parámetros de la función final |
| 10 | `BeginFunctionRetryTimes` | Edm.Int32 | Yes | Begin Function Retry Times | Reintentos de la función inicial |
| 11 | `EndFunctionRetryTimes` | Edm.Int32 | Yes | End Function Retry Times | Reintentos de la función final |
| 12 | `CallbackRunAsUser` | Edm.Int32 | Yes | Callback Run As User | Ejecutar callback como usuario |
| 13 | `StatusMessage` | Edm.String | Yes | Status Message | Mensaje de estado |
| 14 | `RunType` | [BoOBSJRunTypeEnum](../Enums/BoOBSJRunTypeEnum.md) | Yes | Run Type | Tipo de ejecución |
| 15 | `BackendSchedulingSubTasks` | [BackendSchedulingSubTasks](../Tipos-Complejos/BackendSchedulingSubTasks.md) | Yes | Backend Scheduling Sub Tasks | Subtareas de planificación en segundo plano |

## Navigation properties (1)

Use `GET /b1s/v2/ScheduleJobService(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `User` | [User](../Entidades/Users.md) | [Users](Users.md) | CallbackRunAsUser → InternalKey | Usuario |
