# InventoryOpeningBalanceSerialNumber — Números de serie del saldo inicial de inventario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `InventoryOpeningBalanceSerialNumber`
- **Descripción (ES):** Números de serie del saldo inicial de inventario
- **Description (EN):** Inventory Opening Balance Serial Number

- **Properties:** 17

## Properties (17)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocumentEntry` | Edm.Int32 | Yes | Document Entry | Entrada del documento |
| 2 | `ManufacturerSerialNumber` | Edm.String | Yes | Manufacturer Serial Number | Número de serie del fabricante |
| 3 | `InternalSerialNumber` | Edm.String | Yes | Internal Serial Number | Número de serie interno |
| 4 | `ExpiryDate` | Edm.DateTimeOffset | Yes | Expiry Date | Fecha de vencimiento |
| 5 | `ManufactureDate` | Edm.DateTimeOffset | Yes | Manufacture Date | Fecha de fabricación |
| 6 | `ReceptionDate` | Edm.DateTimeOffset | Yes | Reception Date | Fecha de recepción |
| 7 | `WarrantyStart` | Edm.DateTimeOffset | Yes | Warranty Start | Inicio de la garantía |
| 8 | `WarrantyEnd` | Edm.DateTimeOffset | Yes | Warranty End | Fin de la garantía |
| 9 | `Location` | Edm.String | Yes | Location | Ubicación |
| 10 | `Notes` | Edm.String | Yes | Notes | Notas |
| 11 | `BatchID` | Edm.String | Yes | Batch ID | ID de lote |
| 12 | `SystemSerialNumber` | Edm.Int32 | Yes | System Serial Number | Número de serie del sistema |
| 13 | `BaseLineNumber` | Edm.Int32 | Yes | Base Line Number | Número de línea base |
| 14 | `Quantity` | Edm.Double | Yes | Quantity | Cantidad |
| 15 | `TrackingNote` | Edm.Int32 | Yes | Tracking Note | Nota de seguimiento |
| 16 | `TrackingNoteLine` | Edm.Int32 | Yes | Tracking Note Line | Línea de la nota de seguimiento |
| 17 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |

## Used by (properties)

- [InventoryOpeningBalanceLine](InventoryOpeningBalanceLine.md).`InventoryOpeningBalanceSerialNumbers`
