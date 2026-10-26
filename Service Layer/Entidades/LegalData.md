# LegalData — Datos legales

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `LegalData`
- **Descripción (ES):** Datos legales
- **Entity type:** `LegalData`
- **Key:** `DocEntry` (Edm.Int32)
- **DB tables (main / lines):** [OLGL](../../Tablas%20SAP%20B1/OLGL.md), [LGL1](../../Tablas%20SAP%20B1/LGL1.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 15 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/LegalData?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/LegalData/$count` | Contar |
| Get by key | `GET /b1s/v2/LegalData(1)` | Obtener por clave |
| Create | `POST /b1s/v2/LegalData` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/LegalData(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/LegalData(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/LegalData(1)` (only if the B1 object allows removal) | Borrar |

## Properties (15)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` 🔑 | Edm.Int32 | No | Document Entry | DocEntry (clave interna del documento) |
| 2 | `SourceObjectType` | [BoAPARDocumentTypes](../Enums/BoAPARDocumentTypes.md) | Yes | Source Object Type | Tipo de objeto de origen |
| 3 | `SourceObjectEntry` | Edm.Int32 | Yes | Source Object Entry | Entrada del objeto de origen |
| 4 | `DateOfPrinting` | Edm.DateTimeOffset | Yes | Date Of Printing | Fecha de impresión |
| 5 | `TimeOfPrinting` | Edm.TimeOfDay | Yes | Time Of Printing | Hora de impresión |
| 6 | `PrinterBrand` | Edm.String | Yes | Printer Brand | Marca de impresora |
| 7 | `PrinterType` | Edm.String | Yes | Printer Type | Tipo de impresora |
| 8 | `PrinterModel` | Edm.String | Yes | Printer Model | Modelo de impresora |
| 9 | `PrinterFirmwareVersion` | Edm.String | Yes | Printer Firmware Version | Versión de firmware de la impresora |
| 10 | `PrinterDllVersion` | Edm.String | Yes | Printer Dll Version | Versión de DLL de la impresora |
| 11 | `FiscalSeries` | Edm.String | Yes | Fiscal Series | Serie fiscal |
| 12 | `FiscalNumber` | Edm.String | Yes | Fiscal Number | Número fiscal |
| 13 | `DocumentNumber` | Edm.String | Yes | Document Number | Número de documento |
| 14 | `FiscalUserID` | Edm.Int32 | Yes | Fiscal User ID | ID fiscal del usuario |
| 15 | `LegalDataDetailCollection` | Collection([LegalDataDetail](../Tipos-Complejos/LegalDataDetail.md)) | Yes | Legal Data Detail Collection | Colección de detalles de datos legales |

## Navigation properties (1)

Use `GET /b1s/v2/LegalData(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `User` | [User](../Entidades/Users.md) | [Users](Users.md) | FiscalUserID → InternalKey | Usuario |
