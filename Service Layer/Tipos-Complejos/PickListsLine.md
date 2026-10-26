# PickListsLine — Líneas de la lista de picking

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `PickListsLine`
- **Descripción (ES):** Líneas de la lista de picking
- **Description (EN):** Pick Lists Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 12

## Properties (12)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsoluteEntry` | Edm.Int32 | Yes | Absolute Entry | Entrada absoluta (ID interno) |
| 2 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `OrderEntry` | Edm.Int32 | Yes | Order Entry | Entrada del pedido |
| 4 | `OrderRowID` | Edm.Int32 | Yes | Order Row ID | ID de línea del pedido |
| 5 | `PickedQuantity` | Edm.Double | Yes | Picked Quantity | Cantidad pickeada |
| 6 | `PickStatus` | [BoPickStatus](../Enums/BoPickStatus.md) | Yes | Pick Status | Estado de picking |
| 7 | `ReleasedQuantity` | Edm.Double | Yes | Released Quantity | Cantidad liberada |
| 8 | `PreviouslyReleasedQuantity` | Edm.Double | Yes | Previously Released Quantity | Cantidad liberada previamente |
| 9 | `BaseObjectType` | Edm.Int32 | Yes | Base Object Type | Tipo de objeto base |
| 10 | `SerialNumbers` | Collection([SerialNumber](../Tipos-Complejos/SerialNumber.md)) | Yes | Serial Numbers | Números de serie |
| 11 | `BatchNumbers` | Collection([BatchNumber](../Tipos-Complejos/BatchNumber.md)) | Yes | Batch Numbers | Números de lote |
| 12 | `DocumentLinesBinAllocations` | Collection([DocumentLinesBinAllocation](../Tipos-Complejos/DocumentLinesBinAllocation.md)) | Yes | Document Lines Bin Allocations | Asignaciones de ubicaciones de las líneas |

## Used by (properties)

- [PickList](../Entidades/PickLists.md).`PickListsLines`
