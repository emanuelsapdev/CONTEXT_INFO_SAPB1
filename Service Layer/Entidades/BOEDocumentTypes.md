# BOEDocumentTypes — Tipos de documento de letras de cambio

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `BOEDocumentTypes`
- **Descripción (ES):** Tipos de documento de letras de cambio
- **Entity type:** `BOEDocumentType`
- **Key:** `DocEntry` (Edm.Int32)
- **DB tables (main / lines):** [ODTY](../../Tablas%20SAP%20B1/ODTY.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 3 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/BOEDocumentTypes?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/BOEDocumentTypes/$count` | Contar |
| Get by key | `GET /b1s/v2/BOEDocumentTypes(1)` | Obtener por clave |
| Create | `POST /b1s/v2/BOEDocumentTypes` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/BOEDocumentTypes(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/BOEDocumentTypes(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/BOEDocumentTypes(1)` (only if the B1 object allows removal) | Borrar |

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` 🔑 | Edm.Int32 | No | Document Entry | DocEntry (clave interna del documento) |
| 2 | `DocType` | Edm.String | Yes | Document Type | Tipo de documento (artículos/servicios) |
| 3 | `DocDescription` | Edm.String | Yes | Document Description | Descripción del documento |
