# EmployeePreviousEmpoymentInfo — Empleo anterior del empleado

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EmployeePreviousEmpoymentInfo`
- **Descripción (ES):** Empleo anterior del empleado
- **Description (EN):** Employee Previous Empoyment Information
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 7

## Properties (7)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `EmployeeNo` | Edm.Int32 | Yes | Employee Number | Número de empleado |
| 2 | `LineNum` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `FromDtae` | Edm.DateTimeOffset | Yes | From Dtae | Fecha desde |
| 4 | `ToDate` | Edm.DateTimeOffset | Yes | To Date | Fecha hasta |
| 5 | `Employer` | Edm.String | Yes | Employer | Empleador |
| 6 | `Position` | Edm.String | Yes | Position | Posición/cargo |
| 7 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |

## Used by (properties)

- [EmployeeInfo](../Entidades/EmployeesInfo.md).`EmployeePreviousEmpoymentInfoLines`
