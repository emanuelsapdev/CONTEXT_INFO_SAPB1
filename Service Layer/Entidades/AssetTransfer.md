# AssetTransfer — Transferencia de activos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `AssetTransfer`
- **Descripción (ES):** Transferencia de activos
- **Entity type:** `AssetDocument`
- **Key:** `DocEntry` (Edm.Int32)
- **DB tables (main / lines):** [OFTR](../../Tablas%20SAP%20B1/OFTR.md)
- **ETag / optimistic concurrency:** No
- **Other entity sets with the same type:** [AssetRetirement](AssetRetirement.md), [AssetManualDepreciation](AssetManualDepreciation.md), [AssetCapitalization](AssetCapitalization.md), [AssetCapitalizationCreditMemo](AssetCapitalizationCreditMemo.md)
- **Properties:** 36 · **Navigation properties:** 4 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/AssetTransfer?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/AssetTransfer/$count` | Contar |
| Get by key | `GET /b1s/v2/AssetTransfer(1)` | Obtener por clave |
| Create | `POST /b1s/v2/AssetTransfer` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/AssetTransfer(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/AssetTransfer(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/AssetTransfer(1)` (only if the B1 object allows removal) | Borrar |

## Properties (36)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` 🔑 | Edm.Int32 | No | Document Entry | DocEntry (clave interna del documento) |
| 2 | `DocNum` | Edm.Int32 | Yes | Document Number | Número de documento |
| 3 | `Series` | Edm.Int32 | Yes | Series | Serie de numeración |
| 4 | `PostingDate` | Edm.DateTimeOffset | Yes | Posting Date | Fecha de contabilización |
| 5 | `DocumentDate` | Edm.DateTimeOffset | Yes | Document Date | Fecha del documento |
| 6 | `Status` | [AssetDocumentStatusEnum](../Enums/AssetDocumentStatusEnum.md) | Yes | Status | Estado |
| 7 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 8 | `Reference` | Edm.String | Yes | Reference | Referencia |
| 9 | `Currency` | Edm.String | Yes | Currency | Moneda |
| 10 | `DocumentRate` | Edm.Double | Yes | Document Rate | Tipo de cambio del documento |
| 11 | `DocumentTotal` | Edm.Double | Yes | Document Total | Total del documento |
| 12 | `DocumentTotalFC` | Edm.Double | Yes | Document Total FC (foreign currency) | Total del documento (ME) |
| 13 | `DocumentTotalSC` | Edm.Double | Yes | Document Total SC (system currency) | Total del documento (moneda del sistema) |
| 14 | `AssetValueDate` | Edm.DateTimeOffset | Yes | Asset Value Date | Fecha valor del activo |
| 15 | `DocumentType` | [AssetDocumentTypeEnum](../Enums/AssetDocumentTypeEnum.md) | Yes | Document Type | Tipo de documento |
| 16 | `SummerizeByProjects` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Summerize By Projects | Resumir por proyectos |
| 17 | `SummerizeByDistributionRules` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Summerize By Distribution Rules | Resumir por normas de reparto |
| 18 | `ManualDepreciationType` | Edm.String | Yes | Manual Depreciation Type | Tipo de amortización manual |
| 19 | `HandWritten` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Hand Written | Manual (numeración manual) |
| 20 | `CancellationDate` | Edm.DateTimeOffset | Yes | Cancellation Date | Fecha de cancelación |
| 21 | `DepreciationArea` | Edm.String | Yes | Depreciation Area | Área de amortización |
| 22 | `BPLId` | Edm.Int32 | Yes | Branch ID | ID de sucursal |
| 23 | `Origin` | Edm.Int32 | Yes | Origin | Origen |
| 24 | `LowValueAssetRetirement` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Low Value Asset Retirement | Baja de activos de bajo valor |
| 25 | `CancellationOption` | [ClosingOptionEnum](../Enums/ClosingOptionEnum.md) | Yes | Cancellation Option | Opción de cancelación |
| 26 | `OriginalType` | [AssetOriginalTypeEnum](../Enums/AssetOriginalTypeEnum.md) | Yes | Original Type | Tipo original |
| 27 | `BaseReference` | Edm.String | Yes | Base Reference | Referencia base |
| 28 | `BPLName` | Edm.String | Yes | Branch Name | Nombre de la sucursal |
| 29 | `VATRegNum` | Edm.String | Yes | VAT Reg Number | Número de registro de IVA |
| 30 | `AssetDocumentLineCollection` | Collection([AssetDocumentLine](../Tipos-Complejos/AssetDocumentLine.md)) | Yes | Asset Document Line Collection | Colección de líneas del documento de activo |
| 31 | `AssetDocumentAreaJournalCollection` | Collection([AssetDocumentAreaJournal](../Tipos-Complejos/AssetDocumentAreaJournal.md)) | Yes | Asset Document Area Journal Collection | Colección de asientos por área del documento de activo |
| 32 | `PTICode` | Edm.String | Yes | PTI Code | Código PTI |
| 33 | `Letter` | Edm.String | Yes | Letter | Carta |
| 34 | `FolNumFrom` | Edm.Int32 | Yes | Fol Number From | Folio desde |
| 35 | `FolNumTo` | Edm.Int32 | Yes | Fol Number To | Folio hasta |
| 36 | `AssetDocumentNewLocCollection` | Collection([AssetDocumentNewLoc](../Tipos-Complejos/AssetDocumentNewLoc.md)) | Yes | Asset Document New Loc Collection | Colección de nuevas ubicaciones del documento de activo |

## Navigation properties (4)

Use `GET /b1s/v2/AssetTransfer(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Currency2` | [Currency](../Entidades/Currencies.md) | [Currencies](Currencies.md) | Currency → Code | Monedas |
| `DepreciationType` | [DepreciationType](../Entidades/DepreciationTypes.md) | [DepreciationTypes](DepreciationTypes.md) | ManualDepreciationType → Code | Tipo de amortización |
| `DepreciationArea2` | [DepreciationArea](../Entidades/DepreciationAreas.md) | [DepreciationAreas](DepreciationAreas.md) | DepreciationArea → Code | Áreas de amortización |
| `BusinessPlace` | [BusinessPlace](../Entidades/BusinessPlaces.md) | [BusinessPlaces](BusinessPlaces.md) | BPLId → BPLID | Lugar de negocios |
