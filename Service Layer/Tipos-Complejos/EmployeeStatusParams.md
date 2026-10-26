# EmployeeStatusParams — Parámetros de estados de empleados

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EmployeeStatusParams`
- **Descripción (ES):** Parámetros de estados de empleados
- **Description (EN):** Employee Status Parameters

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `StatusId` | Edm.Int32 | Yes | Status ID | ID de estado |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `Description` | Edm.String | Yes | Description | Descripción |

## Used by (service operations)

- [`EmployeeStatusService_GetList`](../Servicios/EmployeeStatusService.md#employeestatusservice_getlist)
