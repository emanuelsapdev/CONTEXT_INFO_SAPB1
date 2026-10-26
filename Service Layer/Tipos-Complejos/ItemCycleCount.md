# ItemCycleCount — Recuentos cíclicos del artículo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ItemCycleCount`
- **Descripción (ES):** Recuentos cíclicos del artículo
- **Description (EN):** Item Cycle Count
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 6

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `CycleCode` | Edm.Int32 | Yes | Cycle Code | Código de ciclo |
| 2 | `Alert` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Alert | Alerta |
| 3 | `NextCountingDate` | Edm.DateTimeOffset | Yes | Next Counting Date | Siguiente fecha de recuento |
| 4 | `AlertTime` | Edm.TimeOfDay | Yes | Alert Time | Hora de la alerta |
| 5 | `DestinationUser` | Edm.Int32 | Yes | Destination User | Usuario destinatario |
| 6 | `WarehouseCode` | Edm.String | Yes | Warehouse Code | Código de almacén |

## Used by (properties)

- [ItemWarehouseInfo](ItemWarehouseInfo.md).`ItemCycleCounts`
