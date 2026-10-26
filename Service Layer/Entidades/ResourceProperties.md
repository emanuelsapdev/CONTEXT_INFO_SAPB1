# ResourceProperties — Propiedades de recursos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ResourceProperties`
- **Descripción (ES):** Propiedades de recursos
- **Entity type:** `ResourceProperty`
- **Key:** `Code` (Edm.Int32)
- **DB tables (main / lines):** [ORSG](../../Tablas%20SAP%20B1/ORSG.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 2 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ResourceProperties?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ResourceProperties/$count` | Contar |
| Get by key | `GET /b1s/v2/ResourceProperties(1)` | Obtener por clave |
| Create | `POST /b1s/v2/ResourceProperties` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ResourceProperties(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ResourceProperties(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/ResourceProperties(1)` (only if the B1 object allows removal) | Borrar |

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.Int32 | No | Code | Código |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
