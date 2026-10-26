# ElectronicFileFormats — Formatos de archivo electrónico

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ElectronicFileFormats`
- **Descripción (ES):** Formatos de archivo electrónico
- **Entity type:** `ElectronicFileFormat`
- **Key:** `FormatID` (Edm.Int32)
- **DB tables (main / lines):** [OFRM](../../Tablas%20SAP%20B1/OFRM.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 8 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ElectronicFileFormats?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ElectronicFileFormats/$count` | Contar |
| Get by key | `GET /b1s/v2/ElectronicFileFormats(1)` | Obtener por clave |
| Create | `POST /b1s/v2/ElectronicFileFormats` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ElectronicFileFormats(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ElectronicFileFormats(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/ElectronicFileFormats(1)` (only if the B1 object allows removal) | Borrar |

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `FormatID` 🔑 | Edm.Int32 | No | Format ID | ID de formato |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `Description` | Edm.String | Yes | Description | Descripción |
| 4 | `Version` | Edm.String | Yes | Version | Versión |
| 5 | `SchemaVersion` | Edm.String | Yes | Schema Version | Versión del esquema |
| 6 | `OutputFilePath` | Edm.String | Yes | Output File Path | Ruta del archivo de salida |
| 7 | `MenuName` | Edm.String | Yes | Menu Name | Nombre del menú |
| 8 | `MenuPath` | Edm.String | Yes | Menu Path | Ruta del menú |

## Navigation properties (2)

Use `GET /b1s/v2/ElectronicFileFormats(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `ImportDeterminations` | Collection([ImportDetermination](../Entidades/ImportDeterminations.md)) | [ImportDeterminations](ImportDeterminations.md) |  | Determinaciones de importación |
| `ExportDeterminations` | Collection([ExportDetermination](../Entidades/ExportDeterminations.md)) | [ExportDeterminations](ExportDeterminations.md) |  | Determinaciones de exportación |
