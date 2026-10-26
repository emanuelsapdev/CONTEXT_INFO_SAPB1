# AssetRevaluationLine — Línea de revalorización de activos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `AssetRevaluationLine`
- **Descripción (ES):** Línea de revalorización de activos
- **Description (EN):** Asset Revaluation Line

- **Properties:** 13

## Properties (13)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 2 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `AssetNumber` | Edm.String | Yes | Asset Number | Número de activo |
| 4 | `CurrentNBV` | Edm.Double | Yes | Current NBV | Valor neto contable actual |
| 5 | `NewNBV` | Edm.Double | Yes | New NBV | Nuevo valor neto contable |
| 6 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 7 | `RevaluationPercent` | Edm.Double | Yes | Revaluation Percent | Porcentaje de revalorización |
| 8 | `DistributionRule` | Edm.String | Yes | Distribution Rule | Norma de reparto |
| 9 | `DistributionRule2` | Edm.String | Yes | Distribution Rule 2 | Norma de reparto 2 |
| 10 | `DistributionRule3` | Edm.String | Yes | Distribution Rule 3 | Norma de reparto 3 |
| 11 | `DistributionRule4` | Edm.String | Yes | Distribution Rule 4 | Norma de reparto 4 |
| 12 | `DistributionRule5` | Edm.String | Yes | Distribution Rule 5 | Norma de reparto 5 |
| 13 | `Project` | Edm.String | Yes | Project | Proyecto |

## Used by (properties)

- [AssetRevaluation](../Entidades/AssetRevaluations.md).`AssetRevaluationLineCollection`
