# PM_WorkOrderData — Gestión de proyectos - Orden de trabajo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `PM_WorkOrderData`
- **Descripción (ES):** Gestión de proyectos - Orden de trabajo
- **Description (EN):** PM Work Order Data
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineID` | Edm.Int32 | Yes | Line ID | ID de línea |
| 2 | `StageID` | Edm.Int32 | Yes | Stage ID | ID de etapa |
| 3 | `DocNumber` | Edm.Int32 | Yes | Document Number | Número de documento |
| 4 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |

## Used by (properties)

- [PM_ProjectDocumentData](../Entidades/ProjectManagements.md).`PM_WorkOrdersCollection`
