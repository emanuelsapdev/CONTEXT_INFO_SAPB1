# EmployeePosition — Puestos de empleados

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `EmployeePosition`
- **Descripción (ES):** Puestos de empleados
- **Entity type:** `EmployeePosition`
- **Key:** `PositionID` (Edm.Int32)
- **DB tables (main / lines):** [OHPS](../../Tablas%20SAP%20B1/OHPS.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 3 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/EmployeePosition?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/EmployeePosition/$count` | Contar |
| Get by key | `GET /b1s/v2/EmployeePosition(1)` | Obtener por clave |
| Create | `POST /b1s/v2/EmployeePosition` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/EmployeePosition(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/EmployeePosition(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/EmployeePosition(1)` (only if the B1 object allows removal) | Borrar |

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `PositionID` 🔑 | Edm.Int32 | No | Position ID | ID de puesto |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `Description` | Edm.String | Yes | Description | Descripción |

## Navigation properties (1)

Use `GET /b1s/v2/EmployeePosition(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `EmployeesInfo` | Collection([EmployeeInfo](../Entidades/EmployeesInfo.md)) | [EmployeesInfo](EmployeesInfo.md) |  | Empleados |
