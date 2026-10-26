# SerialNumber — Número de serie

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `SerialNumber`
- **Descripción (ES):** Número de serie
- **Description (EN):** Serial Number
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 16

## Properties (16)

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
| 14 | `TrackingNote` | Edm.Int32 | Yes | Tracking Note | Nota de seguimiento |
| 15 | `TrackingNoteLine` | Edm.Int32 | Yes | Tracking Note Line | Línea de la nota de seguimiento |
| 16 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |

## Used by (properties)

- [DocumentLine](DocumentLine.md).`SerialNumbers`
- [PickListsLine](PickListsLine.md).`SerialNumbers`
- [ProductionOrderLine](ProductionOrderLine.md).`SerialNumbers`
- [StockTransferLine](StockTransferLine.md).`SerialNumbers`
