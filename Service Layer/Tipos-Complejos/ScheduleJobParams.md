# ScheduleJobParams — Parámetros de trabajos programados

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ScheduleJobParams`
- **Descripción (ES):** Parámetros de trabajos programados
- **Description (EN):** Schedule Job Parameters
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 14

## Properties (14)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `JobID` | Edm.Int32 | Yes | Job ID | ID de trabajo |
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

## Used by (service operations)

- [`ScheduleJobService_GetList`](../Servicios/ScheduleJobService.md#schedulejobservice_getlist)
