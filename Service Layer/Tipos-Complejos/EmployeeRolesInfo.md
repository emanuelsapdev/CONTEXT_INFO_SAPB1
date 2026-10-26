# EmployeeRolesInfo — Funciones del empleado

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EmployeeRolesInfo`
- **Descripción (ES):** Funciones del empleado
- **Description (EN):** Employee Roles Information
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `EmployeeID` | Edm.Int32 | Yes | Employee ID | ID de empleado |
| 2 | `LineNum` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `RoleID` | Edm.Int32 | Yes | Role ID | ID de función |

## Used by (properties)

- [EmployeeInfo](../Entidades/EmployeesInfo.md).`EmployeeRolesInfoLines`
