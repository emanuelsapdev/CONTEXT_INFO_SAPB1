# PMS_DocumentData — Subproyecto - Datos de documento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `PMS_DocumentData`
- **Descripción (ES):** Subproyecto - Datos de documento
- **Description (EN):** PMS Document Data
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 11

## Properties (11)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineID` | Edm.Int32 | Yes | Line ID | ID de línea |
| 2 | `StageID` | Edm.Int32 | Yes | Stage ID | ID de etapa |
| 3 | `DocType` | [PMDocumentTypeEnum](../Enums/PMDocumentTypeEnum.md) | Yes | Document Type | Tipo de documento (artículos/servicios) |
| 4 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 5 | `DocDate` | Edm.DateTimeOffset | Yes | Document Date | Fecha de contabilización del documento |
| 6 | `Total` | Edm.Double | Yes | Total | Total |
| 7 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 8 | `Status` | [LineStatusTypeEnum](../Enums/LineStatusTypeEnum.md) | Yes | Status | Estado |
| 9 | `AmountCategory` | [AmountCatTypeEnum](../Enums/AmountCatTypeEnum.md) | Yes | Amount Category | Categoría de importe |
| 10 | `Categorize` | [PMCategorizeTypeEnum](../Enums/PMCategorizeTypeEnum.md) | Yes | Categorize | Categorizar |
| 11 | `Operation` | [PMOperationTypeEnum](../Enums/PMOperationTypeEnum.md) | Yes | Operation | Operación |

## Used by (properties)

- [PM_SubprojectDocumentData](PM_SubprojectDocumentData.md).`PMS_DocumentsCollection`
