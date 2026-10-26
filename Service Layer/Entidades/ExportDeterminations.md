# ExportDeterminations — Determinaciones de exportación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ExportDeterminations`
- **Descripción (ES):** Determinaciones de exportación
- **Entity type:** `ExportDetermination` (open type: accepts dynamic/UDF properties)
- **Key:** `AbsEntry` (Edm.Int32)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 11 · **Navigation properties:** 3 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ExportDeterminations?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ExportDeterminations/$count` | Contar |
| Get by key | `GET /b1s/v2/ExportDeterminations(1)` | Obtener por clave |
| Create | `POST /b1s/v2/ExportDeterminations` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ExportDeterminations(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ExportDeterminations(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/ExportDeterminations(1)` (only if the B1 object allows removal) | Borrar |

## Properties (11)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` 🔑 | Edm.Int32 | No | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `Code` | [ElectronicDocProtocolCodeStrEnum](../Enums/ElectronicDocProtocolCodeStrEnum.md) | Yes | Code | Código |
| 3 | `Priority` | Edm.Int32 | Yes | Priority | Prioridad |
| 4 | `BusinessPartner` | Edm.String | Yes | Business Partner | Socio de negocios |
| 5 | `Country` | Edm.String | Yes | Country | País |
| 6 | `Series` | Edm.Int32 | Yes | Series | Serie de numeración |
| 7 | `DocumentType` | Edm.String | Yes | Document Type | Tipo de documento |
| 8 | `ExportFormat` | Edm.Int32 | Yes | Export Format | Formato de exportación |
| 9 | `PathFileName` | Edm.String | Yes | Path File Name | Ruta y nombre de archivo |
| 10 | `DocumentSubType` | Edm.String | Yes | Document Sub Type | Subtipo de documento |
| 11 | `VersionNumber` | Edm.Int32 | Yes | Version Number | Número de versión |

## Navigation properties (3)

Use `GET /b1s/v2/ExportDeterminations(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `BusinessPartner2` | [BusinessPartner](../Entidades/BusinessPartners.md) | [BusinessPartners](BusinessPartners.md) | BusinessPartner → CardCode | Socios de negocios |
| `Country2` | [Country](../Entidades/Countries.md) | [Countries](Countries.md) | Country → Code | Países/Regiones |
| `ElectronicFileFormat` | [ElectronicFileFormat](../Entidades/ElectronicFileFormats.md) | [ElectronicFileFormats](ElectronicFileFormats.md) | ExportFormat → FormatID | Formatos de archivo electrónico |

## Service operations that use this type

- [`ExportDeterminationService_GetDeterminations`](../Servicios/ExportDeterminationService.md#exportdeterminationservice_getdeterminations)
