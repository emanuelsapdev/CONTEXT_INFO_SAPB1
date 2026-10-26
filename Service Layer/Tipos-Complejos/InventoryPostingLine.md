# InventoryPostingLine — Líneas de la contabilización de inventario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `InventoryPostingLine`
- **Descripción (ES):** Líneas de la contabilización de inventario
- **Description (EN):** Inventory Posting Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 44

## Properties (44)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocumentEntry` | Edm.Int32 | Yes | Document Entry | Entrada del documento |
| 2 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |
| 4 | `ItemDescription` | Edm.String | Yes | Item Description | Descripción del artículo |
| 5 | `WarehouseCode` | Edm.String | Yes | Warehouse Code | Código de almacén |
| 6 | `BinEntry` | Edm.Int32 | Yes | Bin Entry | Entrada de ubicación |
| 7 | `InWarehouseQuantity` | Edm.Double | Yes | In Warehouse Quantity | Cantidad en almacén |
| 8 | `BarCode` | Edm.String | Yes | Bar Code | Código de barras |
| 9 | `Variance` | Edm.Double | Yes | Variance | Desviación |
| 10 | `VariancePercentage` | Edm.Double | Yes | Variance Percentage | Porcentaje de desviación |
| 11 | `CountedQuantity` | Edm.Double | Yes | Counted Quantity | Cantidad contada |
| 12 | `Price` | Edm.Double | Yes | Price | Precio |
| 13 | `Currency` | Edm.String | Yes | Currency | Moneda |
| 14 | `Total` | Edm.Double | Yes | Total | Total |
| 15 | `VisualOrder` | Edm.Int32 | Yes | Visual Order | Orden visual |
| 16 | `CountDate` | Edm.DateTimeOffset | Yes | Count Date | Fecha de recuento |
| 17 | `CountTime` | Edm.TimeOfDay | Yes | Count Time | Hora de recuento |
| 18 | `BaseEntry` | Edm.Int32 | Yes | Base Entry | Entrada base (DocEntry del documento base) |
| 19 | `BaseLine` | Edm.Int32 | Yes | Base Line | Línea base (LineNum del documento base) |
| 20 | `BaseType` | Edm.Int32 | Yes | Base Type | Tipo base (tipo de objeto del documento base) |
| 21 | `BaseReference` | Edm.String | Yes | Base Reference | Referencia base |
| 22 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 23 | `InventoryOffsetIncreaseAccount` | Edm.String | Yes | Inventory Offset Increase Account | Contracuenta de aumento de inventario |
| 24 | `InventoryOffsetDecreaseAccount` | Edm.String | Yes | Inventory Offset Decrease Account | Contracuenta de disminución de inventario |
| 25 | `ProjectCode` | Edm.String | Yes | Project Code | Código de proyecto |
| 26 | `Manufacturer` | Edm.Int32 | Yes | Manufacturer | Fabricante |
| 27 | `SupplierCatalogNo` | Edm.String | Yes | Supplier Catalog Number | N.º de catálogo del proveedor |
| 28 | `PreferredVendor` | Edm.String | Yes | Preferred Vendor | Proveedor preferido |
| 29 | `CostingCode` | Edm.String | Yes | Costing Code | Norma de reparto (dimensión 1) |
| 30 | `CostingCode2` | Edm.String | Yes | Costing Code 2 | Norma de reparto (dimensión 2) |
| 31 | `CostingCode3` | Edm.String | Yes | Costing Code 3 | Norma de reparto (dimensión 3) |
| 32 | `CostingCode4` | Edm.String | Yes | Costing Code 4 | Norma de reparto (dimensión 4) |
| 33 | `CostingCode5` | Edm.String | Yes | Costing Code 5 | Norma de reparto (dimensión 5) |
| 34 | `UoMCode` | Edm.String | Yes | Uo M Code | Código de unidad de medida |
| 35 | `UoMCountedQuantity` | Edm.Double | Yes | Uo M Counted Quantity | Cantidad contada en unidad de medida |
| 36 | `ItemsPerUnit` | Edm.Double | Yes | Items Per Unit | Artículos por unidad |
| 37 | `AllowBinNegativeQuantity` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Allow Bin Negative Quantity | Permitir cantidad negativa en ubicación |
| 38 | `ActualPrice` | Edm.Double | Yes | Actual Price | Precio real |
| 39 | `PostedValueLC` | Edm.Double | Yes | Posted Value LC (local currency) | Valor contabilizado (moneda local) |
| 40 | `PostedValueSC` | Edm.Double | Yes | Posted Value SC (system currency) | Valor contabilizado (moneda del sistema) |
| 41 | `InventoryPostingLineUoMs` | Collection([InventoryPostingLineUoM](../Tipos-Complejos/InventoryPostingLineUoM.md)) | Yes | Inventory Posting Line Uo Ms | Unidades de medida de líneas de la contabilización |
| 42 | `InventoryPostingSerialNumbers` | Collection([InventoryPostingSerialNumber](../Tipos-Complejos/InventoryPostingSerialNumber.md)) | Yes | Inventory Posting Serial Numbers | Números de serie de la contabilización de inventario |
| 43 | `InventoryPostingBatchNumbers` | Collection([InventoryPostingBatchNumber](../Tipos-Complejos/InventoryPostingBatchNumber.md)) | Yes | Inventory Posting Batch Numbers | Números de lote de la contabilización de inventario |
| 44 | `InventoryPostingCCDNumbers` | Collection([InventoryPostingCCDNumber](../Tipos-Complejos/InventoryPostingCCDNumber.md)) | Yes | Inventory Posting CCD Numbers | Números de declaración aduanera de la contabilización |

## Used by (properties)

- [InventoryPosting](../Entidades/InventoryPostings.md).`InventoryPostingLines`
