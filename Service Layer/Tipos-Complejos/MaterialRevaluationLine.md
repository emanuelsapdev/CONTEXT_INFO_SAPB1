# MaterialRevaluationLine — Líneas de la revalorización de inventario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `MaterialRevaluationLine`
- **Descripción (ES):** Líneas de la revalorización de inventario
- **Description (EN):** Material Revaluation Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 21

## Properties (21)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineNum` | Edm.Int32 | Yes | Line Number | Número de línea |
| 2 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |
| 3 | `ItemDescription` | Edm.String | Yes | Item Description | Descripción del artículo |
| 4 | `Quantity` | Edm.Double | Yes | Quantity | Cantidad |
| 5 | `Price` | Edm.Double | Yes | Price | Precio |
| 6 | `WarehouseCode` | Edm.String | Yes | Warehouse Code | Código de almacén |
| 7 | `ActualPrice` | Edm.Double | Yes | Actual Price | Precio real |
| 8 | `OnHand` | Edm.Double | Yes | On Hand | En stock |
| 9 | `DebitCredit` | Edm.Double | Yes | Debit Credit | Debe/haber |
| 10 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 11 | `RevaluationDecrementAccount` | Edm.String | Yes | Revaluation Decrement Account | Cuenta de disminución por revalorización |
| 12 | `RevaluationIncrementAccount` | Edm.String | Yes | Revaluation Increment Account | Cuenta de aumento por revalorización |
| 13 | `RevalAmountToStock` | Edm.Double | Yes | Reval Amount To Stock | Importe de revalorización a stock |
| 14 | `Project` | Edm.String | Yes | Project | Proyecto |
| 15 | `DistributionRule` | Edm.String | Yes | Distribution Rule | Norma de reparto |
| 16 | `DistributionRule2` | Edm.String | Yes | Distribution Rule 2 | Norma de reparto 2 |
| 17 | `DistributionRule3` | Edm.String | Yes | Distribution Rule 3 | Norma de reparto 3 |
| 18 | `DistributionRule4` | Edm.String | Yes | Distribution Rule 4 | Norma de reparto 4 |
| 19 | `DistributionRule5` | Edm.String | Yes | Distribution Rule 5 | Norma de reparto 5 |
| 20 | `FIFOLayers` | Collection([FIFOLayer](../Tipos-Complejos/FIFOLayer.md)) | Yes | FIFO Layers | Capas FIFO |
| 21 | `SNBLinesCollection` | Collection([SNBLines](../Tipos-Complejos/SNBLines.md)) | Yes | Serial and Batch Lines Collection | Colección de líneas de series y lotes |

## Used by (properties)

- [MaterialRevaluation](../Entidades/MaterialRevaluation.md).`MaterialRevaluationLines`
