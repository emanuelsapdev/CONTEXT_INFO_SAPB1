# StockTakings — Toma de inventario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `StockTakings`
- **Descripción (ES):** Toma de inventario
- **Entity type:** `StockTaking` (open type: accepts dynamic/UDF properties)
- **Key:** `ItemCode` (Edm.String), `WarehouseCode` (Edm.String)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 3 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/StockTakings?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/StockTakings/$count` | Contar |
| Get by key | `GET /b1s/v2/StockTakings(ItemCode='value',WarehouseCode='value')` | Obtener por clave |
| Create | `POST /b1s/v2/StockTakings` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/StockTakings(ItemCode='value',WarehouseCode='value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/StockTakings(ItemCode='value',WarehouseCode='value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/StockTakings(ItemCode='value',WarehouseCode='value')` (only if the B1 object allows removal) | Borrar |

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ItemCode` 🔑 | Edm.String | No | Item Code | Código de artículo |
| 2 | `WarehouseCode` 🔑 | Edm.String | No | Warehouse Code | Código de almacén |
| 3 | `Counted` | Edm.Double | Yes | Counted | Contado |

## Navigation properties (2)

Use `GET /b1s/v2/StockTakings(ItemCode='value',WarehouseCode='value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Item` | [Item](../Entidades/Items.md) | [Items](Items.md) | ItemCode → ItemCode | Artículos |
| `Warehouse` | [Warehouse](../Entidades/Warehouses.md) | [Warehouses](Warehouses.md) | WarehouseCode → WarehouseCode | Almacén |
