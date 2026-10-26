# PM_ActivityData — Gestión de proyectos - Actividad

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `PM_ActivityData`
- **Descripción (ES):** Gestión de proyectos - Actividad
- **Description (EN):** PM Activity Data
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineID` | Edm.Int32 | Yes | Line ID | ID de línea |
| 2 | `StageID` | Edm.Int32 | Yes | Stage ID | ID de etapa |
| 3 | `ActivityID` | Edm.Int32 | Yes | Activity ID | ID de actividad |

## Used by (properties)

- [PM_ProjectDocumentData](../Entidades/ProjectManagements.md).`PM_ActivitiesCollection`
