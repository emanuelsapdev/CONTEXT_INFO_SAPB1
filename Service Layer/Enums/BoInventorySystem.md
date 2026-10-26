# BoInventorySystem — Método de valoración de inventario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoInventorySystem`
- **Descripción (ES):** Método de valoración de inventario
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `bis_MovingAverage` | 0 | Moving Average | Precio promedio ponderado |
| `bis_Standard` | 1 | Standard | Estándar |
| `bis_FIFO` | 2 | FIFO | FIFO |
| `bis_SNB` | 3 | Serial and Batch | Por número de serie/lote |

## Used by (3 properties)

- [AdminInfo](../Tipos-Complejos/AdminInfo.md).`ContinuousStockSystem`
- [Item](../Entidades/Items.md).`CostAccountingMethod`
- [ItemGroups](../Entidades/ItemGroups.md).`InventorySystem`
