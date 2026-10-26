# CertificateSeries — Series de certificados

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `CertificateSeries`
- **Descripción (ES):** Series de certificados
- **Entity type:** `CertificateSeries`
- **Key:** `AbsEntry` (Edm.Int32)
- **DB tables (main / lines):** [OCSN](../../Tablas%20SAP%20B1/OCSN.md), [CSN1](../../Tablas%20SAP%20B1/CSN1.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 6 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/CertificateSeries?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/CertificateSeries/$count` | Contar |
| Get by key | `GET /b1s/v2/CertificateSeries(1)` | Obtener por clave |
| Create | `POST /b1s/v2/CertificateSeries` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/CertificateSeries(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/CertificateSeries(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/CertificateSeries(1)` (only if the B1 object allows removal) | Borrar |

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` 🔑 | Edm.Int32 | No | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `Code` | Edm.String | Yes | Code | Código |
| 3 | `Section` | Edm.Int32 | Yes | Section | Sección |
| 4 | `Location` | Edm.Int32 | Yes | Location | Ubicación |
| 5 | `DefaultSeries` | Edm.Int32 | Yes | Default Series | Serie predeterminada |
| 6 | `SeriesLines` | Collection([SeriesLine](../Tipos-Complejos/SeriesLine.md)) | Yes | Series Lines | Líneas de la serie |

## Navigation properties (2)

Use `GET /b1s/v2/CertificateSeries(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Section2` | [Section](../Entidades/Sections.md) | [Sections](Sections.md) | Section → AbsEntry | Secciones |
| `WarehouseLocation` | [WarehouseLocation](../Entidades/WarehouseLocations.md) | [WarehouseLocations](WarehouseLocations.md) | Location → Code | Ubicaciones de almacenes |
