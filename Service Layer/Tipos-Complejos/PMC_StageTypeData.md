# PMC_StageTypeData — Gestión de proyectos (config.) - Datos de tipo de etapa

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `PMC_StageTypeData`
- **Descripción (ES):** Gestión de proyectos (config.) - Datos de tipo de etapa
- **Description (EN):** PMC Stage Type Data

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `StageID` | Edm.Int32 | Yes | Stage ID | ID de etapa |
| 2 | `StageName` | Edm.String | Yes | Stage Name | Nombre de la etapa |
| 3 | `StageDescription` | Edm.String | Yes | Stage Description | Descripción de la etapa |

## Used by (service operations)

- [`ProjectManagementConfigurationService_AddStageTypes`](../Servicios/ProjectManagementConfigurationService.md#projectmanagementconfigurationservice_addstagetypes)
- [`ProjectManagementConfigurationService_DeleteStageTypes`](../Servicios/ProjectManagementConfigurationService.md#projectmanagementconfigurationservice_deletestagetypes)
- [`ProjectManagementConfigurationService_GetStageTypes`](../Servicios/ProjectManagementConfigurationService.md#projectmanagementconfigurationservice_getstagetypes)
- [`ProjectManagementConfigurationService_UpdateStageTypes`](../Servicios/ProjectManagementConfigurationService.md#projectmanagementconfigurationservice_updatestagetypes)
