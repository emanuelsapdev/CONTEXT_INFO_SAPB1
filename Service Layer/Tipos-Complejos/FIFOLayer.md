# FIFOLayer — Capas FIFO

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `FIFOLayer`
- **Descripción (ES):** Capas FIFO
- **Description (EN):** FIFO Layer
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 6

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TransactionSequenceNum` | Edm.Int32 | Yes | Transaction Sequence Number | Número de secuencia de transacción |
| 2 | `LayerID` | Edm.Int32 | Yes | Layer ID | ID de capa |
| 3 | `Quantity` | Edm.Double | Yes | Quantity | Cantidad |
| 4 | `Price` | Edm.Double | Yes | Price | Precio |
| 5 | `LineTotal` | Edm.Double | Yes | Line Total | Total de línea |
| 6 | `BaseLine` | Edm.Int32 | Yes | Base Line | Línea base (LineNum del documento base) |

## Used by (properties)

- [MaterialRevaluationLine](MaterialRevaluationLine.md).`FIFOLayers`
