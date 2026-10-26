# AssetRevaluations — Revalorizaciones de activos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `AssetRevaluations`
- **Descripción (ES):** Revalorizaciones de activos
- **Entity type:** `AssetRevaluation`
- **Key:** `DocEntry` (Edm.Int32)
- **DB tables (main / lines):** [OFAR](../../Tablas%20SAP%20B1/OFAR.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 21 · **Navigation properties:** 3 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/AssetRevaluations?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/AssetRevaluations/$count` | Contar |
| Get by key | `GET /b1s/v2/AssetRevaluations(1)` | Obtener por clave |
| Create | `POST /b1s/v2/AssetRevaluations` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/AssetRevaluations(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/AssetRevaluations(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/AssetRevaluations(1)` (only if the B1 object allows removal) | Borrar |

## Properties (21)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` 🔑 | Edm.Int32 | No | Document Entry | DocEntry (clave interna del documento) |
| 2 | `DocNum` | Edm.Int32 | Yes | Document Number | Número de documento |
| 3 | `Series` | Edm.Int32 | Yes | Series | Serie de numeración |
| 4 | `PostingDate` | Edm.DateTimeOffset | Yes | Posting Date | Fecha de contabilización |
| 5 | `AssetValueDate` | Edm.DateTimeOffset | Yes | Asset Value Date | Fecha valor del activo |
| 6 | `Reference` | Edm.String | Yes | Reference | Referencia |
| 7 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 8 | `JournalRemarks` | Edm.String | Yes | Journal Remarks | Comentarios del asiento |
| 9 | `DepreciationArea` | Edm.String | Yes | Depreciation Area | Área de amortización |
| 10 | `TransId` | Edm.Int32 | Yes | Trans ID | ID de transacción (asiento) |
| 11 | `HandWritten` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Hand Written | Manual (numeración manual) |
| 12 | `PeriodIndicator` | Edm.String | Yes | Period Indicator | Indicador de período |
| 13 | `DocumentDate` | Edm.DateTimeOffset | Yes | Document Date | Fecha del documento |
| 14 | `BPLId` | Edm.Int32 | Yes | Branch ID | ID de sucursal |
| 15 | `BPLName` | Edm.String | Yes | Branch Name | Nombre de la sucursal |
| 16 | `VATRegNum` | Edm.String | Yes | VAT Reg Number | Número de registro de IVA |
| 17 | `RevaluationPercent` | Edm.Double | Yes | Revaluation Percent | Porcentaje de revalorización |
| 18 | `IfrsPosting` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Ifrs Posting | Contabilización NIIF |
| 19 | `SummerizeByProjects` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Summerize By Projects | Resumir por proyectos |
| 20 | `SummerizeByDistributionRules` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Summerize By Distribution Rules | Resumir por normas de reparto |
| 21 | `AssetRevaluationLineCollection` | Collection([AssetRevaluationLine](../Tipos-Complejos/AssetRevaluationLine.md)) | Yes | Asset Revaluation Line Collection | Colección de líneas de revalorización de activos |

## Navigation properties (3)

Use `GET /b1s/v2/AssetRevaluations(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `DepreciationArea2` | [DepreciationArea](../Entidades/DepreciationAreas.md) | [DepreciationAreas](DepreciationAreas.md) | DepreciationArea → Code | Áreas de amortización |
| `JournalEntry` | [JournalEntry](../Entidades/JournalEntries.md) | [JournalEntries](JournalEntries.md) | TransId → JdtNum | Asientos contables |
| `BusinessPlace` | [BusinessPlace](../Entidades/BusinessPlaces.md) | [BusinessPlaces](BusinessPlaces.md) | BPLId → BPLID | Lugar de negocios |
