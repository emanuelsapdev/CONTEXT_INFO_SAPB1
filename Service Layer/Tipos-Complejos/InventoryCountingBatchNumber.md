# InventoryCountingBatchNumber — Números de lote del recuento de inventario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `InventoryCountingBatchNumber`
- **Descripción (ES):** Números de lote del recuento de inventario
- **Description (EN):** Inventory Counting Batch Number

- **Properties:** 18

## Properties (18)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `BatchNumber` | Edm.String | Yes | Batch Number | Número de lote |
| 2 | `ManufacturerSerialNumber` | Edm.String | Yes | Manufacturer Serial Number | Número de serie del fabricante |
| 3 | `InternalSerialNumber` | Edm.String | Yes | Internal Serial Number | Número de serie interno |
| 4 | `ExpiryDate` | Edm.DateTimeOffset | Yes | Expiry Date | Fecha de vencimiento |
| 5 | `ManufactureDate` | Edm.DateTimeOffset | Yes | Manufacture Date | Fecha de fabricación |
| 6 | `AddmisionDate` | Edm.DateTimeOffset | Yes | Addmision Date | Fecha de admisión |
| 7 | `Location` | Edm.String | Yes | Location | Ubicación |
| 8 | `Notes` | Edm.String | Yes | Notes | Notas |
| 9 | `Quantity` | Edm.Double | Yes | Quantity | Cantidad |
| 10 | `BaseLineNumber` | Edm.Int32 | Yes | Base Line Number | Número de línea base |
| 11 | `DocumentEntry` | Edm.Int32 | Yes | Document Entry | Entrada del documento |
| 12 | `CounterType` | [CounterTypeEnum](../Enums/CounterTypeEnum.md) | Yes | Counter Type | Tipo de contador |
| 13 | `CounterID` | Edm.Int32 | Yes | Counter ID | ID del contador |
| 14 | `MultipleCounterRole` | [MultipleCounterRoleEnum](../Enums/MultipleCounterRoleEnum.md) | Yes | Multiple Counter Role | Rol de contador múltiple |
| 15 | `TrackingNote` | Edm.Int32 | Yes | Tracking Note | Nota de seguimiento |
| 16 | `TrackingNoteLine` | Edm.Int32 | Yes | Tracking Note Line | Línea de la nota de seguimiento |
| 17 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |
| 18 | `SystemSerialNumber` | Edm.Int32 | Yes | System Serial Number | Número de serie del sistema |

## Used by (properties)

- [InventoryCountingLine](InventoryCountingLine.md).`InventoryCountingBatchNumbers`
