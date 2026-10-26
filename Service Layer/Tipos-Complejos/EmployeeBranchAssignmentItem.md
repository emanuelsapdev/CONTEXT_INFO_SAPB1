# EmployeeBranchAssignmentItem — Asignación de sucursal al empleado

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EmployeeBranchAssignmentItem`
- **Descripción (ES):** Asignación de sucursal al empleado
- **Description (EN):** Employee Branch Assignment Item
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `EmployeeID` | Edm.Int32 | Yes | Employee ID | ID de empleado |
| 2 | `BPLID` | Edm.Int32 | Yes | BPLID | ID de sucursal |

## Used by (properties)

- [EmployeeInfo](../Entidades/EmployeesInfo.md).`EmployeeBranchAssignment`
