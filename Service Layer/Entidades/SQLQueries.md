# SQLQueries — Consultas SQL

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `SQLQueries`
- **Descripción (ES):** Consultas SQL
- **Entity type:** `SQLQuery`
- **Key:** `SqlCode` (Edm.String)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 6 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/SQLQueries?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/SQLQueries/$count` | Contar |
| Get by key | `GET /b1s/v2/SQLQueries('value')` | Obtener por clave |
| Create | `POST /b1s/v2/SQLQueries` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/SQLQueries('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/SQLQueries('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/SQLQueries('value')` (only if the B1 object allows removal) | Borrar |

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `SqlCode` 🔑 | Edm.String | No | Sql Code | Código SQL |
| 2 | `SqlName` | Edm.String | Yes | Sql Name | Nombre SQL |
| 3 | `SqlText` | Edm.String | Yes | Sql Text | Texto SQL |
| 4 | `ParamList` | Edm.String | Yes | Parameter List | Lista de parámetros |
| 5 | `CreateDate` | Edm.DateTimeOffset | Yes | Create Date | Fecha de creación |
| 6 | `UpdateDate` | Edm.DateTimeOffset | Yes | Update Date | Fecha de actualización |
