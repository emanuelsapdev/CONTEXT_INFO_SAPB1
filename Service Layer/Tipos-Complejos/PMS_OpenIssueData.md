# PMS_OpenIssueData — Subproyecto - Tema abierto

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `PMS_OpenIssueData`
- **Descripción (ES):** Subproyecto - Tema abierto
- **Description (EN):** PMS Open Issue Data
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 11

## Properties (11)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineID` | Edm.Int32 | Yes | Line ID | ID de línea |
| 2 | `StageID` | Edm.Int32 | Yes | Stage ID | ID de etapa |
| 3 | `Area` | Edm.Int32 | Yes | Area | Área |
| 4 | `Priority` | Edm.Int32 | Yes | Priority | Prioridad |
| 5 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 6 | `Closed` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Closed | Cerrado |
| 7 | `SolutionID` | Edm.Int32 | Yes | Solution ID | ID de solución |
| 8 | `Responsible` | Edm.Int32 | Yes | Responsible | Responsable |
| 9 | `EnteredBy` | Edm.Int32 | Yes | Entered By | Ingresado por |
| 10 | `EnteredDate` | Edm.DateTimeOffset | Yes | Entered Date | Fecha de ingreso |
| 11 | `Effort` | Edm.Double | Yes | Effort | Esfuerzo |

## Used by (properties)

- [PM_SubprojectDocumentData](PM_SubprojectDocumentData.md).`PMS_OpenIssuesCollection`
