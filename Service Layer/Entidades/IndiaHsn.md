# IndiaHsn — India - Códigos HSN

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `IndiaHsn`
- **Descripción (ES):** India - Códigos HSN
- **Entity type:** `IndiaHsn`
- **Key:** `AbsEntry` (Edm.Int32)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 6 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/IndiaHsn?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/IndiaHsn/$count` | Contar |
| Get by key | `GET /b1s/v2/IndiaHsn(1)` | Obtener por clave |
| Create | `POST /b1s/v2/IndiaHsn` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/IndiaHsn(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/IndiaHsn(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/IndiaHsn(1)` (only if the B1 object allows removal) | Borrar |

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` 🔑 | Edm.Int32 | No | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `Chapter` | Edm.String | Yes | Chapter | Capítulo |
| 3 | `Heading` | Edm.String | Yes | Heading | Encabezado |
| 4 | `SubHeading` | Edm.String | Yes | Sub Heading | Subencabezado |
| 5 | `Description` | Edm.String | Yes | Description | Descripción |
| 6 | `ChapterID` | Edm.String | Yes | Chapter ID | ID de capítulo |

## Navigation properties (1)

Use `GET /b1s/v2/IndiaHsn(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Items` | Collection([Item](../Entidades/Items.md)) | [Items](Items.md) |  | Artículos |
