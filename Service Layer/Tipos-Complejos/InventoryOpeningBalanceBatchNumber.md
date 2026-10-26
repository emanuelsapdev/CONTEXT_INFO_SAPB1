# InventoryOpeningBalanceBatchNumber — Números de lote del saldo inicial de inventario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `InventoryOpeningBalanceBatchNumber`
- **Descripción (ES):** Números de lote del saldo inicial de inventario
- **Description (EN):** Inventory Opening Balance Batch Number

- **Properties:** 15

## Properties (15)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocumentEntry` | Edm.Int32 | Yes | Document Entry | Entrada del documento |
| 2 | `BatchNumber` | Edm.String | Yes | Batch Number | Número de lote |
| 3 | `ManufacturerSerialNumber` | Edm.String | Yes | Manufacturer Serial Number | Número de serie del fabricante |
| 4 | `InternalSerialNumber` | Edm.String | Yes | Internal Serial Number | Número de serie interno |
| 5 | `ExpiryDate` | Edm.DateTimeOffset | Yes | Expiry Date | Fecha de vencimiento |
| 6 | `ManufactureDate` | Edm.DateTimeOffset | Yes | Manufacture Date | Fecha de fabricación |
| 7 | `AddmisionDate` | Edm.DateTimeOffset | Yes | Addmision Date | Fecha de admisión |
| 8 | `Location` | Edm.String | Yes | Location | Ubicación |
| 9 | `Notes` | Edm.String | Yes | Notes | Notas |
| 10 | `Quantity` | Edm.Double | Yes | Quantity | Cantidad |
| 11 | `BaseLineNumber` | Edm.Int32 | Yes | Base Line Number | Número de línea base |
| 12 | `TrackingNote` | Edm.Int32 | Yes | Tracking Note | Nota de seguimiento |
| 13 | `TrackingNoteLine` | Edm.Int32 | Yes | Tracking Note Line | Línea de la nota de seguimiento |
| 14 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |
| 15 | `SystemSerialNumber` | Edm.Int32 | Yes | System Serial Number | Número de serie del sistema |

## Used by (properties)

- [InventoryOpeningBalanceLine](InventoryOpeningBalanceLine.md).`InventoryOpeningBalanceBatchNumbers`
