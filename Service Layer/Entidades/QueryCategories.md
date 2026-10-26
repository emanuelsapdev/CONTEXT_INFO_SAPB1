# QueryCategories — Categorías de consultas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `QueryCategories`
- **Descripción (ES):** Categorías de consultas
- **Entity type:** `QueryCategory` (open type: accepts dynamic/UDF properties)
- **Key:** `Code` (Edm.Int32)
- **DB tables (main / lines):** [OQCN](../../Tablas%20SAP%20B1/OQCN.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 3 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/QueryCategories?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/QueryCategories/$count` | Contar |
| Get by key | `GET /b1s/v2/QueryCategories(1)` | Obtener por clave |
| Create | `POST /b1s/v2/QueryCategories` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/QueryCategories(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/QueryCategories(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/QueryCategories(1)` (only if the B1 object allows removal) | Borrar |

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.Int32 | No | Code | Código |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `Permissions` | Edm.String | Yes | Permissions | Permisos |

## Navigation properties (1)

Use `GET /b1s/v2/QueryCategories(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `UserQueries` | Collection([UserQuery](../Entidades/UserQueries.md)) | [UserQueries](UserQueries.md) |  | Consultas de usuario |
