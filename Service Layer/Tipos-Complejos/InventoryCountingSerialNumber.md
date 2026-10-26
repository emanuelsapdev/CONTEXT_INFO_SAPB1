# InventoryCountingSerialNumber — Números de serie del recuento de inventario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `InventoryCountingSerialNumber`
- **Descripción (ES):** Números de serie del recuento de inventario
- **Description (EN):** Inventory Counting Serial Number

- **Properties:** 20

## Properties (20)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ManufacturerSerialNumber` | Edm.String | Yes | Manufacturer Serial Number | Número de serie del fabricante |
| 2 | `InternalSerialNumber` | Edm.String | Yes | Internal Serial Number | Número de serie interno |
| 3 | `ExpiryDate` | Edm.DateTimeOffset | Yes | Expiry Date | Fecha de vencimiento |
| 4 | `ManufactureDate` | Edm.DateTimeOffset | Yes | Manufacture Date | Fecha de fabricación |
| 5 | `ReceptionDate` | Edm.DateTimeOffset | Yes | Reception Date | Fecha de recepción |
| 6 | `WarrantyStart` | Edm.DateTimeOffset | Yes | Warranty Start | Inicio de la garantía |
| 7 | `WarrantyEnd` | Edm.DateTimeOffset | Yes | Warranty End | Fin de la garantía |
| 8 | `Location` | Edm.String | Yes | Location | Ubicación |
| 9 | `Notes` | Edm.String | Yes | Notes | Notas |
| 10 | `BatchID` | Edm.String | Yes | Batch ID | ID de lote |
| 11 | `SystemSerialNumber` | Edm.Int32 | Yes | System Serial Number | Número de serie del sistema |
| 12 | `BaseLineNumber` | Edm.Int32 | Yes | Base Line Number | Número de línea base |
| 13 | `Quantity` | Edm.Double | Yes | Quantity | Cantidad |
| 14 | `DocumentEntry` | Edm.Int32 | Yes | Document Entry | Entrada del documento |
| 15 | `CounterType` | [CounterTypeEnum](../Enums/CounterTypeEnum.md) | Yes | Counter Type | Tipo de contador |
| 16 | `CounterID` | Edm.Int32 | Yes | Counter ID | ID del contador |
| 17 | `MultipleCounterRole` | [MultipleCounterRoleEnum](../Enums/MultipleCounterRoleEnum.md) | Yes | Multiple Counter Role | Rol de contador múltiple |
| 18 | `TrackingNote` | Edm.Int32 | Yes | Tracking Note | Nota de seguimiento |
| 19 | `TrackingNoteLine` | Edm.Int32 | Yes | Tracking Note Line | Línea de la nota de seguimiento |
| 20 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |

## Used by (properties)

- [InventoryCountingLine](InventoryCountingLine.md).`InventoryCountingSerialNumbers`
