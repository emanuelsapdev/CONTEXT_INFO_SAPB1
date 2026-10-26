# WorkflowTask — Tarea de flujo de trabajo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `WorkflowTask`
- **Descripción (ES):** Tarea de flujo de trabajo
- **Description (EN):** Workflow Task

- **Properties:** 14

## Properties (14)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `InstanceID` | Edm.Int32 | Yes | Instance ID | ID de instancia |
| 2 | `TaskID` | Edm.Int32 | Yes | Task ID | ID de tarea |
| 3 | `TemplateID` | Edm.String | Yes | Template ID | ID de plantilla |
| 4 | `TemplateName` | Edm.String | Yes | Template Name | Nombre de la plantilla |
| 5 | `Description` | Edm.String | Yes | Description | Descripción |
| 6 | `Operation` | Edm.String | Yes | Operation | Operación |
| 7 | `Type` | Edm.String | Yes | Type | Tipo |
| 8 | `Owner` | Edm.String | Yes | Owner | Titular |
| 9 | `Priority` | Edm.Int32 | Yes | Priority | Prioridad |
| 10 | `Status` | Edm.String | Yes | Status | Estado |
| 11 | `Name` | Edm.String | Yes | Name | Nombre |
| 12 | `WorkflowTaskInputObjectCollection` | Collection([WorkflowTaskInputObject](../Tipos-Complejos/WorkflowTaskInputObject.md)) | Yes | Workflow Task Input Object Collection | Objetos de entrada de la tarea de flujo de trabajo |
| 13 | `WorkflowTaskNoteCollection` | Collection([WorkflowTaskNote](../Tipos-Complejos/WorkflowTaskNote.md)) | Yes | Workflow Task Note Collection | Notas de la tarea de flujo de trabajo |
| 14 | `WorkflowTaskOutputObjectCollection` | Collection([WorkflowTaskOutputObject](../Tipos-Complejos/WorkflowTaskOutputObject.md)) | Yes | Workflow Task Output Object Collection | Objetos de salida de la tarea de flujo de trabajo |

## Used by (service operations)

- [`WorkflowTaskService_GetApprovalTaskList`](../Servicios/WorkflowTaskService.md#workflowtaskservice_getapprovaltasklist)
