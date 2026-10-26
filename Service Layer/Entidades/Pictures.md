# Pictures — Imágenes

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `Pictures`
- **Descripción (ES):** Imágenes
- **Entity type:** `Picture`
- **Key:** `PictureName` (Edm.String)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 5 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/Pictures?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/Pictures/$count` | Contar |
| Get by key | `GET /b1s/v2/Pictures('value')` | Obtener por clave |
| Create | `POST /b1s/v2/Pictures` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/Pictures('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/Pictures('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/Pictures('value')` (only if the B1 object allows removal) | Borrar |

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `PictureName` 🔑 | Edm.String | No | Picture Name | Nombre de la imagen |
| 2 | `PicturePath` | Edm.String | No | Picture Path | Ruta de la imagen |
| 3 | `PictureSize` | Edm.Int32 | No | Picture Size | Tamaño de la imagen |
| 4 | `PictureCreateDate` | Edm.String | No | Picture Create Date | Fecha de creación de la imagen |
| 5 | `PictureModifyDate` | Edm.String | No | Picture Modify Date | Fecha de modificación de la imagen |
