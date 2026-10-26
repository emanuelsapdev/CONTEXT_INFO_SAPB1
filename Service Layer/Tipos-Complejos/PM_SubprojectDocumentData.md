# PM_SubprojectDocumentData — Gestión de proyectos - Datos de subproyecto

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `PM_SubprojectDocumentData`
- **Descripción (ES):** Gestión de proyectos - Datos de subproyecto
- **Description (EN):** PM Subproject Document Data
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 24

## Properties (24)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` | Edm.Int32 | Yes | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `Owner` | Edm.Int32 | Yes | Owner | Titular |
| 3 | `SubprojectName` | Edm.String | Yes | Subproject Name | Nombre del subproyecto |
| 4 | `StartDate` | Edm.DateTimeOffset | Yes | Start Date | Fecha de inicio |
| 5 | `FinishedPercent` | Edm.Double | Yes | Finished Percent | Porcentaje completado |
| 6 | `ParentID` | Edm.Int32 | Yes | Parent ID | ID del padre |
| 7 | `ProjectID` | Edm.Int32 | Yes | Project ID | ID de proyecto |
| 8 | `Order` | Edm.Int32 | Yes | Order | Pedido / orden |
| 9 | `SubprojectType` | Edm.Int32 | Yes | Subproject Type | Tipo de subproyecto |
| 10 | `SubprojectContribution` | Edm.Double | Yes | Subproject Contribution | Contribución del subproyecto |
| 11 | `SubprojectStatus` | [SubprojectStatusTypeEnum](../Enums/SubprojectStatusTypeEnum.md) | Yes | Subproject Status | Estado del subproyecto |
| 12 | `SubprojectEndDate` | Edm.DateTimeOffset | Yes | Subproject End Date | Fecha de fin del subproyecto |
| 13 | `ActualCost` | Edm.Double | Yes | Actual Cost | Costo real |
| 14 | `PlannedCost` | Edm.Double | Yes | Planned Cost | Costo planificado |
| 15 | `SubprojectDepth` | Edm.Int32 | Yes | Subproject Depth | Profundidad del subproyecto |
| 16 | `DueDate` | Edm.DateTimeOffset | Yes | Due Date | Fecha de vencimiento |
| 17 | `PMS_StagesCollection` | Collection([PMS_StageData](../Tipos-Complejos/PMS_StageData.md)) | Yes | PMS Stages Collection | Colección de etapas del subproyecto |
| 18 | `PMS_OpenIssuesCollection` | Collection([PMS_OpenIssueData](../Tipos-Complejos/PMS_OpenIssueData.md)) | Yes | PMS Open Issues Collection | Colección de temas abiertos del subproyecto |
| 19 | `PMS_DocumentsCollection` | Collection([PMS_DocumentData](../Tipos-Complejos/PMS_DocumentData.md)) | Yes | PMS Documents Collection | Colección de documentos del subproyecto |
| 20 | `PMS_ActivitiesCollection` | Collection([PMS_ActivityData](../Tipos-Complejos/PMS_ActivityData.md)) | Yes | PMS Activities Collection | Colección de actividades del subproyecto |
| 21 | `PMS_WorkOrdersCollection` | Collection([PMS_WorkOrderData](../Tipos-Complejos/PMS_WorkOrderData.md)) | Yes | PMS Work Orders Collection | Colección de órdenes de trabajo del subproyecto |
| 22 | `PMS_SummaryData` | [PMS_SummaryData](../Tipos-Complejos/PMS_SummaryData.md) | Yes | PMS Summary Data | Datos de resumen del subproyecto |
| 23 | `PMS_DocAttachements` | Collection([PMS_DocAttachement](../Tipos-Complejos/PMS_DocAttachement.md)) | Yes | PMS Document Attachements | Anexos del documento del subproyecto |
| 24 | `PMS_StageAttachements` | Collection([PMS_StageAttachement](../Tipos-Complejos/PMS_StageAttachement.md)) | Yes | PMS Stage Attachements | Anexos de etapas del subproyecto |

## Used by (service operations)

- [`ProjectManagementService_AddSubproject`](../Servicios/ProjectManagementService.md#projectmanagementservice_addsubproject)
- [`ProjectManagementService_GetSubproject`](../Servicios/ProjectManagementService.md#projectmanagementservice_getsubproject)
- [`ProjectManagementService_UpdateSubproject`](../Servicios/ProjectManagementService.md#projectmanagementservice_updatesubproject)
