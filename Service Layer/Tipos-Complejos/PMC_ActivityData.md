# PMC_ActivityData — Gestión de proyectos (config.) - Datos de tipo de actividad

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `PMC_ActivityData`
- **Descripción (ES):** Gestión de proyectos (config.) - Datos de tipo de actividad
- **Description (EN):** PMC Activity Data

- **Properties:** 5

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ActivityID` | Edm.Int32 | Yes | Activity ID | ID de actividad |
| 2 | `ActivityType` | Edm.String | Yes | Activity Type | Tipo de actividad |
| 3 | `LaborItem` | Edm.String | Yes | Labor Item | Artículo de mano de obra |
| 4 | `IsChargeable` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Chargeable | Es facturable |
| 5 | `IsAbsence` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Absence | Es ausencia |

## Used by (service operations)

- [`ProjectManagementConfigurationService_AddActivities`](../Servicios/ProjectManagementConfigurationService.md#projectmanagementconfigurationservice_addactivities)
- [`ProjectManagementConfigurationService_DeleteActivities`](../Servicios/ProjectManagementConfigurationService.md#projectmanagementconfigurationservice_deleteactivities)
- [`ProjectManagementConfigurationService_GetActivities`](../Servicios/ProjectManagementConfigurationService.md#projectmanagementconfigurationservice_getactivities)
- [`ProjectManagementConfigurationService_UpdateActivities`](../Servicios/ProjectManagementConfigurationService.md#projectmanagementconfigurationservice_updateactivities)
