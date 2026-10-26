# WebClientPreferences — Cliente web - Preferencias

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `WebClientPreferences`
- **Descripción (ES):** Cliente web - Preferencias
- **Entity type:** `WebClientPreference`
- **Key:** `Guid` (Edm.String)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 5 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/WebClientPreferences?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/WebClientPreferences/$count` | Contar |
| Get by key | `GET /b1s/v2/WebClientPreferences('value')` | Obtener por clave |
| Create | `POST /b1s/v2/WebClientPreferences` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/WebClientPreferences('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/WebClientPreferences('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/WebClientPreferences('value')` (only if the B1 object allows removal) | Borrar |

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Guid` 🔑 | Edm.String | No | Guid | GUID |
| 2 | `UserId` | Edm.Int32 | Yes | User ID | ID de usuario |
| 3 | `TableName` | Edm.String | Yes | Table Name | Nombre de la tabla |
| 4 | `ColumnName` | Edm.String | Yes | Column Name | Nombre de columna |
| 5 | `DefaultValue` | Edm.String | Yes | Default Value | Valor predeterminado |
