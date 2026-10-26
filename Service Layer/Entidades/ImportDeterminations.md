# ImportDeterminations — Determinaciones de importación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ImportDeterminations`
- **Descripción (ES):** Determinaciones de importación
- **Entity type:** `ImportDetermination` (open type: accepts dynamic/UDF properties)
- **Key:** `AbsEntry` (Edm.Int32)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 10 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ImportDeterminations?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ImportDeterminations/$count` | Contar |
| Get by key | `GET /b1s/v2/ImportDeterminations(1)` | Obtener por clave |
| Create | `POST /b1s/v2/ImportDeterminations` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ImportDeterminations(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ImportDeterminations(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/ImportDeterminations(1)` (only if the B1 object allows removal) | Borrar |

## Properties (10)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` 🔑 | Edm.Int32 | No | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `Code` | [ElectronicDocProtocolCodeStrEnum](../Enums/ElectronicDocProtocolCodeStrEnum.md) | Yes | Code | Código |
| 3 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 4 | `ObjectType` | Edm.String | Yes | Object Type | Tipo de objeto |
| 5 | `ObjectTypeXPath` | Edm.String | Yes | Object Type X Path | Tipo de objeto XPath |
| 6 | `FieldType` | [ImportFieldTypeEnum](../Enums/ImportFieldTypeEnum.md) | Yes | Field Type | Tipo de campo |
| 7 | `FieldTypeXPath` | Edm.String | Yes | Field Type X Path | Tipo de campo XPath |
| 8 | `ImportFormat` | Edm.Int32 | Yes | Import Format | Formato de importación |
| 9 | `DefaultDigitalSeries` | Edm.Int32 | Yes | Default Digital Series | Serie digital predeterminada |
| 10 | `VersionNumber` | Edm.Int32 | Yes | Version Number | Número de versión |

## Navigation properties (1)

Use `GET /b1s/v2/ImportDeterminations(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `ElectronicFileFormat` | [ElectronicFileFormat](../Entidades/ElectronicFileFormats.md) | [ElectronicFileFormats](ElectronicFileFormats.md) | ImportFormat → FormatID | Formatos de archivo electrónico |

## Service operations that use this type

- [`ImportDeterminationService_GetDeterminations`](../Servicios/ImportDeterminationService.md#importdeterminationservice_getdeterminations)
