# BatchNumber — Número de lote

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `BatchNumber`
- **Descripción (ES):** Número de lote
- **Description (EN):** Batch Number
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 14

## Properties (14)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `BatchNumberProperty` | Edm.String | Yes | Batch Number Property | Propiedad del número de lote |
| 2 | `ManufacturerSerialNumber` | Edm.String | Yes | Manufacturer Serial Number | Número de serie del fabricante |
| 3 | `InternalSerialNumber` | Edm.String | Yes | Internal Serial Number | Número de serie interno |
| 4 | `ExpiryDate` | Edm.DateTimeOffset | Yes | Expiry Date | Fecha de vencimiento |
| 5 | `ManufacturingDate` | Edm.DateTimeOffset | Yes | Manufacturing Date | Fecha de fabricación |
| 6 | `AddmisionDate` | Edm.DateTimeOffset | Yes | Addmision Date | Fecha de admisión |
| 7 | `Location` | Edm.String | Yes | Location | Ubicación |
| 8 | `Notes` | Edm.String | Yes | Notes | Notas |
| 9 | `Quantity` | Edm.Double | Yes | Quantity | Cantidad |
| 10 | `BaseLineNumber` | Edm.Int32 | Yes | Base Line Number | Número de línea base |
| 11 | `TrackingNote` | Edm.Int32 | Yes | Tracking Note | Nota de seguimiento |
| 12 | `TrackingNoteLine` | Edm.Int32 | Yes | Tracking Note Line | Línea de la nota de seguimiento |
| 13 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |
| 14 | `SystemSerialNumber` | Edm.Int32 | Yes | System Serial Number | Número de serie del sistema |

## Used by (properties)

- [DocumentLine](DocumentLine.md).`BatchNumbers`
- [PickListsLine](PickListsLine.md).`BatchNumbers`
- [ProductionOrderLine](ProductionOrderLine.md).`BatchNumbers`
- [StockTransferLine](StockTransferLine.md).`BatchNumbers`
