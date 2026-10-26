# WebClientBookmarkTiles — Cliente web - Mosaicos de marcadores

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `WebClientBookmarkTiles`
- **Descripción (ES):** Cliente web - Mosaicos de marcadores
- **Entity type:** `WebClientBookmarkTile`
- **Key:** `Guid` (Edm.String)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 7 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/WebClientBookmarkTiles?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/WebClientBookmarkTiles/$count` | Contar |
| Get by key | `GET /b1s/v2/WebClientBookmarkTiles('value')` | Obtener por clave |
| Create | `POST /b1s/v2/WebClientBookmarkTiles` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/WebClientBookmarkTiles('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/WebClientBookmarkTiles('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/WebClientBookmarkTiles('value')` (only if the B1 object allows removal) | Borrar |

## Properties (7)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Guid` 🔑 | Edm.String | No | Guid | GUID |
| 2 | `Title` | Edm.String | Yes | Title | Título |
| 3 | `SubTitle` | Edm.String | Yes | Sub Title | Subtítulo |
| 4 | `Info` | Edm.String | Yes | Information | Información |
| 5 | `BindType` | Edm.String | Yes | Bind Type | Tipo de vinculación |
| 6 | `UrlTarget` | Edm.String | Yes | Url Target | Destino de URL |
| 7 | `Endpoint` | Edm.String | Yes | Endpoint | Endpoint |
