# BoProductionOrderOriginEnum — Origen de la orden de fabricación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoProductionOrderOriginEnum`
- **Descripción (ES):** Origen de la orden de fabricación
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `bopooManual` | 0 | Manual | Manual |
| `bopooMRP` | 1 | MRP | MRP |
| `bopooSalesOrder` | 2 | Sales Order | Pedido de cliente |
| `bopooProductionOrder` | 3 | Production Order | Orden de fabricación |

## Used by (1 properties)

- [ProductionOrder](../Entidades/ProductionOrders.md).`ProductionOrderOrigin`
