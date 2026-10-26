# SQLViews — Vistas SQL

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `SQLViews`
- **Descripción (ES):** Vistas SQL
- **Entity type:** `SQLView`
- **Key:** `Name` (Edm.String)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 4 · **Navigation properties:** 0 · **Bound actions:** 2

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/SQLViews?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/SQLViews/$count` | Contar |
| Get by key | `GET /b1s/v2/SQLViews('value')` | Obtener por clave |
| Create | `POST /b1s/v2/SQLViews` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/SQLViews('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/SQLViews('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/SQLViews('value')` (only if the B1 object allows removal) | Borrar |
| Action `Expose` | `POST /b1s/v2/SQLViews('value')/Expose` | Exponer (publicar vista) |
| Action `Unexpose` | `POST /b1s/v2/SQLViews('value')/Unexpose` | Dejar de exponer (vista) |

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Name` 🔑 | Edm.String | No | Name | Nombre |
| 2 | `DBType` | Edm.String | Yes | DB Type | Tipo de base de datos |
| 3 | `SchemaName` | Edm.String | Yes | Schema Name | Nombre del esquema |
| 4 | `CreateDate` | Edm.DateTimeOffset | Yes | Create Date | Fecha de creación |

## Bound actions (2)

### Expose

- **Descripción (ES):** Exponer (publicar vista)
- **Request:** `POST /b1s/v2/SQLViews('value')/Expose`

### Unexpose

- **Descripción (ES):** Dejar de exponer (vista)
- **Request:** `POST /b1s/v2/SQLViews('value')/Unexpose`

