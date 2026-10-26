# PMS_ActivityData — Subproyecto - Datos de actividad

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `PMS_ActivityData`
- **Descripción (ES):** Subproyecto - Datos de actividad
- **Description (EN):** PMS Activity Data
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineID` | Edm.Int32 | Yes | Line ID | ID de línea |
| 2 | `StageID` | Edm.Int32 | Yes | Stage ID | ID de etapa |
| 3 | `ActivityID` | Edm.Int32 | Yes | Activity ID | ID de actividad |

## Used by (properties)

- [PM_SubprojectDocumentData](PM_SubprojectDocumentData.md).`PMS_ActivitiesCollection`
