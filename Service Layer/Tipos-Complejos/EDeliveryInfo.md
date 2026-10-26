# EDeliveryInfo — Información de entrega electrónica

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EDeliveryInfo`
- **Descripción (ES):** Información de entrega electrónica
- **Description (EN):** E Delivery Information

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 2 | `MoveType` | Edm.Int32 | Yes | Move Type | Tipo de movimiento |
| 3 | `VehicleNo` | Edm.String | Yes | Vehicle Number | Número de vehículo |

## Used by (properties)

- [Document](../Entidades/PurchaseQuotations.md).`EDeliveryInfo`
- [StockTransfer](../Entidades/StockTransfers.md).`EDeliveryInfo`
