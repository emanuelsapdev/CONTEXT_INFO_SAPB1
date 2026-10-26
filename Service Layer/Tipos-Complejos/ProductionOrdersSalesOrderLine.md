# ProductionOrdersSalesOrderLine — Líneas de pedido de cliente de la orden de fabricación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ProductionOrdersSalesOrderLine`
- **Descripción (ES):** Líneas de pedido de cliente de la orden de fabricación
- **Description (EN):** Production Orders Sales Order Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 2 | `BaseNumber` | Edm.Int32 | Yes | Base Number | Número base |
| 3 | `BaseAbsEntry` | Edm.Int32 | Yes | Base Abs Entry | Entrada absoluta base |
| 4 | `BaseLine` | Edm.Int32 | Yes | Base Line | Línea base (LineNum del documento base) |

## Used by (properties)

- [ProductionOrder](../Entidades/ProductionOrders.md).`ProductionOrdersSalesOrderLines`
