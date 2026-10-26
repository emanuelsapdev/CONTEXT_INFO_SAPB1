# AssetDocumentLine — Línea del documento de activo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `AssetDocumentLine`
- **Descripción (ES):** Línea del documento de activo
- **Description (EN):** Asset Document Line

- **Properties:** 20

## Properties (20)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 2 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `AssetNumber` | Edm.String | Yes | Asset Number | Número de activo |
| 4 | `GLAccount` | Edm.String | Yes | G/L Account | Cuenta de mayor |
| 5 | `Quantity` | Edm.Double | Yes | Quantity | Cantidad |
| 6 | `TotalLC` | Edm.Double | Yes | Total LC (local currency) | Total (moneda local) |
| 7 | `TotalFC` | Edm.Double | Yes | Total FC (foreign currency) | Total (ME) |
| 8 | `TotalSC` | Edm.Double | Yes | Total SC (system currency) | Total (moneda del sistema) |
| 9 | `DepreciationArea` | Edm.String | Yes | Depreciation Area | Área de amortización |
| 10 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 11 | `NewAssetNumber` | Edm.String | Yes | New Asset Number | Nuevo número de activo |
| 12 | `Partial` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Partial | Parcial |
| 13 | `APC` | Edm.Double | Yes | APC | APC |
| 14 | `NewAssetClass` | Edm.String | Yes | New Asset Class | Nueva clase de activo |
| 15 | `DistributionRule` | Edm.String | Yes | Distribution Rule | Norma de reparto |
| 16 | `DistributionRule2` | Edm.String | Yes | Distribution Rule 2 | Norma de reparto 2 |
| 17 | `DistributionRule3` | Edm.String | Yes | Distribution Rule 3 | Norma de reparto 3 |
| 18 | `DistributionRule4` | Edm.String | Yes | Distribution Rule 4 | Norma de reparto 4 |
| 19 | `DistributionRule5` | Edm.String | Yes | Distribution Rule 5 | Norma de reparto 5 |
| 20 | `Project` | Edm.String | Yes | Project | Proyecto |

## Used by (properties)

- [AssetDocument](../Entidades/AssetRetirement.md).`AssetDocumentLineCollection`
