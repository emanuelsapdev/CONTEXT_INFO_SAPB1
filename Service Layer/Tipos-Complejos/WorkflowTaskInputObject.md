# WorkflowTaskInputObject — Objeto de entrada de tarea de flujo de trabajo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `WorkflowTaskInputObject`
- **Descripción (ES):** Objeto de entrada de tarea de flujo de trabajo
- **Description (EN):** Workflow Task Input Object

- **Properties:** 6

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TaskID` | Edm.Int32 | Yes | Task ID | ID de tarea |
| 2 | `LineId` | Edm.Int32 | Yes | Line ID | ID de línea |
| 3 | `Type` | Edm.String | Yes | Type | Tipo |
| 4 | `Key` | Edm.String | Yes | Key | Clave |
| 5 | `SubType` | Edm.String | Yes | Sub Type | Subtipo |
| 6 | `Detail` | Edm.String | Yes | Detail | Detalle |

## Used by (properties)

- [WorkflowTask](WorkflowTask.md).`WorkflowTaskInputObjectCollection`
