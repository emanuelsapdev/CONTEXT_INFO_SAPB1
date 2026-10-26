# EmployeeAbsenceInfo — Ausencia del empleado

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EmployeeAbsenceInfo`
- **Descripción (ES):** Ausencia del empleado
- **Description (EN):** Employee Absence Information
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 7

## Properties (7)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `EmployeeID` | Edm.Int32 | Yes | Employee ID | ID de empleado |
| 2 | `LineNum` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `FromDate` | Edm.DateTimeOffset | Yes | From Date | Fecha desde |
| 4 | `ToDate` | Edm.DateTimeOffset | Yes | To Date | Fecha hasta |
| 5 | `Reason` | Edm.String | Yes | Reason | Motivo |
| 6 | `ApprovedBy` | Edm.String | Yes | Approved By | Autorizado por |
| 7 | `ConfirmerNumber` | Edm.Int32 | Yes | Confirmer Number | Número del confirmador |

## Used by (properties)

- [EmployeeInfo](../Entidades/EmployeesInfo.md).`EmployeeAbsenceInfoLines`
