# WorkflowTaskService — Servicio de tareas de flujo de trabajo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `WorkflowTaskService`
- **Descripción (ES):** Servicio de tareas de flujo de trabajo
- **Operations:** 2

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`WorkflowTaskService_Complete`](#workflowtaskservice_complete) | action | — | Complete | Completar |
| [`WorkflowTaskService_GetApprovalTaskList`](#workflowtaskservice_getapprovaltasklist) | action | Collection([WorkflowTask](../Tipos-Complejos/WorkflowTask.md)) | Get Approval Task List | Obtener lista de tareas de autorización |

## WorkflowTaskService_Complete

- **Descripción (ES):** Completar
- **Request:** `POST /b1s/v2/WorkflowTaskService_Complete`
- **Parameters:** `WorkflowTaskCompleteParams` ([WorkflowTaskCompleteParams](../Tipos-Complejos/WorkflowTaskCompleteParams.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "WorkflowTaskCompleteParams": {
    "TaskID": 0,
    "Note": "string",
    "TriggerParams": "string"
  }
}
```

## WorkflowTaskService_GetApprovalTaskList

- **Descripción (ES):** Obtener lista de tareas de autorización
- **Request:** `POST /b1s/v2/WorkflowTaskService_GetApprovalTaskList`
- **Parameters:** `WorkflowApprovalTaskListParams` ([WorkflowApprovalTaskListParams](../Tipos-Complejos/WorkflowApprovalTaskListParams.md))
- **Returns:** Collection([WorkflowTask](../Tipos-Complejos/WorkflowTask.md))

```json
{
  "WorkflowApprovalTaskListParams": {
    "Status": "string"
  }
}
```

