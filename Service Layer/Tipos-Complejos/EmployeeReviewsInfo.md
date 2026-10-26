# EmployeeReviewsInfo — Evaluación del empleado

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EmployeeReviewsInfo`
- **Descripción (ES):** Evaluación del empleado
- **Description (EN):** Employee Reviews Information
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 7

## Properties (7)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `EmployeeNo` | Edm.Int32 | Yes | Employee Number | Número de empleado |
| 2 | `LineNum` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `Date` | Edm.DateTimeOffset | Yes | Date | Fecha |
| 4 | `ReviewDescription` | Edm.String | Yes | Review Description | Descripción de la evaluación |
| 5 | `Manager` | Edm.Int32 | Yes | Manager | Responsable |
| 6 | `Grade` | Edm.String | Yes | Grade | Calificación |
| 7 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |

## Used by (properties)

- [EmployeeInfo](../Entidades/EmployeesInfo.md).`EmployeeReviewsInfoLines`
