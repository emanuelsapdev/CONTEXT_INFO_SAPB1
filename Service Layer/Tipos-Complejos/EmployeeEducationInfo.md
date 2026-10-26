# EmployeeEducationInfo — Formación del empleado

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EmployeeEducationInfo`
- **Descripción (ES):** Formación del empleado
- **Description (EN):** Employee Education Information
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 8

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `EmployeeNo` | Edm.Int32 | Yes | Employee Number | Número de empleado |
| 2 | `LineNum` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `FromDate` | Edm.DateTimeOffset | Yes | From Date | Fecha desde |
| 4 | `ToDate` | Edm.DateTimeOffset | Yes | To Date | Fecha hasta |
| 5 | `EducationType` | Edm.Int32 | Yes | Education Type | Tipo de formación |
| 6 | `Institute` | Edm.String | Yes | Institute | Institución |
| 7 | `Major` | Edm.String | Yes | Major | Mayor |
| 8 | `Diploma` | Edm.String | Yes | Diploma | Diploma |

## Used by (properties)

- [EmployeeInfo](../Entidades/EmployeesInfo.md).`EmployeeEducationInfoLines`
