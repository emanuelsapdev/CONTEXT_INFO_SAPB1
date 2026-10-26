# ItemImages — Imágenes de artículos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ItemImages`
- **Descripción (ES):** Imágenes de artículos
- **Entity type:** `ItemImage`
- **Key:** `ItemCode` (Edm.String)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 2 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ItemImages?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ItemImages/$count` | Contar |
| Get by key | `GET /b1s/v2/ItemImages('value')` | Obtener por clave |
| Create | `POST /b1s/v2/ItemImages` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ItemImages('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ItemImages('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/ItemImages('value')` (only if the B1 object allows removal) | Borrar |

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ItemCode` 🔑 | Edm.String | No | Item Code | Código de artículo |
| 2 | `Picture` | Edm.String | No | Picture | Imagen |
