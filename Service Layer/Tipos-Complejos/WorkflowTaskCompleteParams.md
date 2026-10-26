# WorkflowTaskCompleteParams — Parámetros para completar tarea de flujo de trabajo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `WorkflowTaskCompleteParams`
- **Descripción (ES):** Parámetros para completar tarea de flujo de trabajo
- **Description (EN):** Workflow Task Complete Parameters

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TaskID` | Edm.Int32 | Yes | Task ID | ID de tarea |
| 2 | `Note` | Edm.String | Yes | Note | Nota |
| 3 | `TriggerParams` | Edm.String | Yes | Trigger Parameters | Parámetros de disparo |

## Used by (service operations)

- [`WorkflowTaskService_Complete`](../Servicios/WorkflowTaskService.md#workflowtaskservice_complete)
