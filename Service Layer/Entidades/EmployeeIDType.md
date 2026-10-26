# EmployeeIDType — Tipos de identificación de empleado

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `EmployeeIDType`
- **Descripción (ES):** Tipos de identificación de empleado
- **Entity type:** `EmployeeIDType`
- **Key:** `IDType` (Edm.String)
- **DB tables (main / lines):** [OIDT](../../Tablas%20SAP%20B1/OIDT.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 1 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/EmployeeIDType?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/EmployeeIDType/$count` | Contar |
| Get by key | `GET /b1s/v2/EmployeeIDType('value')` | Obtener por clave |
| Create | `POST /b1s/v2/EmployeeIDType` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/EmployeeIDType('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/EmployeeIDType('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/EmployeeIDType('value')` (only if the B1 object allows removal) | Borrar |

## Properties (1)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `IDType` 🔑 | Edm.String | No | ID Type | Tipo de identificación |

## Navigation properties (1)

Use `GET /b1s/v2/EmployeeIDType('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `EmployeesInfo` | Collection([EmployeeInfo](../Entidades/EmployeesInfo.md)) | [EmployeesInfo](EmployeesInfo.md) |  | Empleados |
