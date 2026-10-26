# DocumentLinesBinAllocation — Asignaciones de ubicaciones de las líneas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DocumentLinesBinAllocation`
- **Descripción (ES):** Asignaciones de ubicaciones de las líneas
- **Description (EN):** Document Lines Bin Allocation
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 5

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `BinAbsEntry` | Edm.Int32 | Yes | Bin Abs Entry | Entrada absoluta de ubicación |
| 2 | `Quantity` | Edm.Double | Yes | Quantity | Cantidad |
| 3 | `AllowNegativeQuantity` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Allow Negative Quantity | Permitir cantidad negativa |
| 4 | `SerialAndBatchNumbersBaseLine` | Edm.Int32 | Yes | Serial And Batch Numbers Base Line | Línea base de números de serie y lote |
| 5 | `BaseLineNumber` | Edm.Int32 | Yes | Base Line Number | Número de línea base |

## Used by (properties)

- [DocumentLine](DocumentLine.md).`DocumentLinesBinAllocations`
- [PickListsLine](PickListsLine.md).`DocumentLinesBinAllocations`
