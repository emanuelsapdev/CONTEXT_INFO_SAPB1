# BackendSchedulingSubTasks — Subtareas de planificación en segundo plano

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `BackendSchedulingSubTasks`
- **Descripción (ES):** Subtareas de planificación en segundo plano
- **Description (EN):** Backend Scheduling Sub Tasks

- **Properties:** 13

## Properties (13)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `JobID` | Edm.Int32 | Yes | Job ID | ID de trabajo |
| 2 | `SubTaskID` | Edm.Int32 | Yes | Sub Task ID | ID de subtarea |
| 3 | `TaskType` | Edm.String | Yes | Task Type | Tipo de tarea |
| 4 | `Parameters` | Edm.String | Yes | Parameters | Parámetros |
| 5 | `RunAsUser` | Edm.Int32 | Yes | Run As User | Ejecutar como usuario |
| 6 | `Status` | [BoBSJ1StatusEnum](../Enums/BoBSJ1StatusEnum.md) | Yes | Status | Estado |
| 7 | `PostTask` | Edm.Int32 | Yes | Post Task | Tarea posterior |
| 8 | `PreTask` | Edm.Int32 | Yes | Pre Task | Tarea previa |
| 9 | `LastRunningDate` | Edm.DateTimeOffset | Yes | Last Running Date | Fecha de la última ejecución |
| 10 | `LastRunningTime` | Edm.TimeOfDay | Yes | Last Running Time | Hora de la última ejecución |
| 11 | `RetryTimes` | Edm.Int32 | Yes | Retry Times | Cantidad de reintentos |
| 12 | `TimeOut` | Edm.Int32 | Yes | Time Out | Tiempo de espera |
| 13 | `StatusMessage` | Edm.String | Yes | Status Message | Mensaje de estado |

## Used by (properties)

- [ScheduleJob](../Entidades/ScheduleJobService.md).`BackendSchedulingSubTasks`
