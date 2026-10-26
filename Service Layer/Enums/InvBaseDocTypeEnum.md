# InvBaseDocTypeEnum — Tipo de documento base de inventario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `InvBaseDocTypeEnum`
- **Descripción (ES):** Tipo de documento base de inventario
- **Underlying type:** Edm.Int32
- **Members:** 6

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `Default` | 0 | Default | Predeterminado |
| `Empty` | 1 | Empty | Vacío |
| `PurchaseDeliveryNotes` | 2 | Purchase Delivery Notes | Pedidos de entrada de mercancías |
| `InventoryGeneralEntry` | 3 | Inventory General Entry | Entradas de mercancías |
| `WarehouseTransfers` | 4 | Warehouse Transfers | Transferencias de stock |
| `InventoryTransferRequest` | 5 | Inventory Transfer Request | Solicitud de transferencia de stock |

## Used by (1 properties)

- [StockTransferLine](../Tipos-Complejos/StockTransferLine.md).`BaseType`
