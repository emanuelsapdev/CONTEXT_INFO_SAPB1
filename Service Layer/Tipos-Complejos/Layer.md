# Layer — Capas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `Layer`
- **Descripción (ES):** Capas
- **Description (EN):** Layer

- **Properties:** 7

## Properties (7)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TransactionSequenceNum` | Edm.Int32 | Yes | Transaction Sequence Number | Número de secuencia de transacción |
| 2 | `LayerID` | Edm.Int32 | Yes | Layer ID | ID de capa |
| 3 | `DocNumber` | Edm.String | Yes | Document Number | Número de documento |
| 4 | `DocType` | [TransTypesEnum](../Enums/TransTypesEnum.md) | Yes | Document Type | Tipo de documento (artículos/servicios) |
| 5 | `EntryDate` | Edm.DateTimeOffset | Yes | Entry Date | Fecha de entrada |
| 6 | `CurrentCost` | Edm.Double | Yes | Current Cost | Costo actual |
| 7 | `OpenQty` | Edm.Double | Yes | Open Quantity | Cantidad abierta |

## Used by (properties)

- [MaterialRevaluationFIFO](MaterialRevaluationFIFO.md).`Layers`
