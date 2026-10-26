# ItemProperties — Propiedades de artículos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ItemProperties`
- **Descripción (ES):** Propiedades de artículos
- **Entity type:** `ItemProperty` (open type: accepts dynamic/UDF properties)
- **Key:** `Number` (Edm.Int32)
- **DB tables (main / lines):** [OITG](../../Tablas%20SAP%20B1/OITG.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 2 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ItemProperties?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ItemProperties/$count` | Contar |
| Get by key | `GET /b1s/v2/ItemProperties(1)` | Obtener por clave |
| Create | `POST /b1s/v2/ItemProperties` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ItemProperties(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ItemProperties(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/ItemProperties(1)` (only if the B1 object allows removal) | Borrar |

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Number` 🔑 | Edm.Int32 | No | Number | Número |
| 2 | `PropertyName` | Edm.String | Yes | Property Name | Nombre de propiedad |
