# PMC_TaskData — Gestión de proyectos (config.) - Datos de tarea

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `PMC_TaskData`
- **Descripción (ES):** Gestión de proyectos (config.) - Datos de tarea
- **Description (EN):** PMC Task Data

- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TaskID` | Edm.Int32 | Yes | Task ID | ID de tarea |
| 2 | `TaskName` | Edm.String | Yes | Task Name | Nombre de la tarea |

## Used by (service operations)

- [`ProjectManagementConfigurationService_AddTasks`](../Servicios/ProjectManagementConfigurationService.md#projectmanagementconfigurationservice_addtasks)
- [`ProjectManagementConfigurationService_DeleteTasks`](../Servicios/ProjectManagementConfigurationService.md#projectmanagementconfigurationservice_deletetasks)
- [`ProjectManagementConfigurationService_GetTasks`](../Servicios/ProjectManagementConfigurationService.md#projectmanagementconfigurationservice_gettasks)
- [`ProjectManagementConfigurationService_UpdateTasks`](../Servicios/ProjectManagementConfigurationService.md#projectmanagementconfigurationservice_updatetasks)
