# DocLinePickList — Listas de picking de la línea del documento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DocLinePickList`
- **Descripción (ES):** Listas de picking de la línea del documento
- **Description (EN):** Document Line Pick List

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `PickListEntry` | Edm.Int32 | Yes | Pick List Entry | Entrada de la lista de picking |
| 2 | `PickListLineNum` | Edm.Int32 | Yes | Pick List Line Number | Línea de la lista de picking |
| 3 | `PickListBatchAndBinLineNum` | Edm.Int32 | Yes | Pick List Batch And Bin Line Number | Línea de lote y ubicación de la lista de picking |

## Used by (properties)

- [DocumentLine](DocumentLine.md).`DocLinePickLists`
- [StockTransferLine](StockTransferLine.md).`DocLinePickLists`
