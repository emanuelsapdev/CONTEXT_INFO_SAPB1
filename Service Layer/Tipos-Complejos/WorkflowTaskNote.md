# WorkflowTaskNote — Nota de tarea de flujo de trabajo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `WorkflowTaskNote`
- **Descripción (ES):** Nota de tarea de flujo de trabajo
- **Description (EN):** Workflow Task Note

- **Properties:** 5

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TaskID` | Edm.Int32 | Yes | Task ID | ID de tarea |
| 2 | `LineId` | Edm.Int32 | Yes | Line ID | ID de línea |
| 3 | `Note` | Edm.String | Yes | Note | Nota |
| 4 | `Creator` | Edm.String | Yes | Creator | Creador |
| 5 | `NoteDate` | Edm.DateTimeOffset | Yes | Note Date | Fecha de la nota |

## Used by (properties)

- [WorkflowTask](WorkflowTask.md).`WorkflowTaskNoteCollection`
