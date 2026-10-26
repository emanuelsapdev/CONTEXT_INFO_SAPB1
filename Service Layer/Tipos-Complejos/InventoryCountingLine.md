# InventoryCountingLine — Líneas del recuento de inventario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `InventoryCountingLine`
- **Descripción (ES):** Líneas del recuento de inventario
- **Description (EN):** Inventory Counting Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 40

## Properties (40)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocumentEntry` | Edm.Int32 | Yes | Document Entry | Entrada del documento |
| 2 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |
| 4 | `ItemDescription` | Edm.String | Yes | Item Description | Descripción del artículo |
| 5 | `Freeze` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Freeze | Congelar |
| 6 | `WarehouseCode` | Edm.String | Yes | Warehouse Code | Código de almacén |
| 7 | `BinEntry` | Edm.Int32 | Yes | Bin Entry | Entrada de ubicación |
| 8 | `InWarehouseQuantity` | Edm.Double | Yes | In Warehouse Quantity | Cantidad en almacén |
| 9 | `Counted` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Counted | Contado |
| 10 | `UoMCode` | Edm.String | Yes | Uo M Code | Código de unidad de medida |
| 11 | `BarCode` | Edm.String | Yes | Bar Code | Código de barras |
| 12 | `UoMCountedQuantity` | Edm.Double | Yes | Uo M Counted Quantity | Cantidad contada en unidad de medida |
| 13 | `ItemsPerUnit` | Edm.Double | Yes | Items Per Unit | Artículos por unidad |
| 14 | `CountedQuantity` | Edm.Double | Yes | Counted Quantity | Cantidad contada |
| 15 | `Variance` | Edm.Double | Yes | Variance | Desviación |
| 16 | `VariancePercentage` | Edm.Double | Yes | Variance Percentage | Porcentaje de desviación |
| 17 | `VisualOrder` | Edm.Int32 | Yes | Visual Order | Orden visual |
| 18 | `TargetEntry` | Edm.Int32 | Yes | Target Entry | Entrada de destino |
| 19 | `TargetLine` | Edm.Int32 | Yes | Target Line | Línea de destino |
| 20 | `TargetType` | Edm.Int32 | Yes | Target Type | Tipo de destino |
| 21 | `TargetReference` | Edm.String | Yes | Target Reference | Referencia de destino |
| 22 | `ProjectCode` | Edm.String | Yes | Project Code | Código de proyecto |
| 23 | `Manufacturer` | Edm.Int32 | Yes | Manufacturer | Fabricante |
| 24 | `SupplierCatalogNo` | Edm.String | Yes | Supplier Catalog Number | N.º de catálogo del proveedor |
| 25 | `PreferredVendor` | Edm.String | Yes | Preferred Vendor | Proveedor preferido |
| 26 | `CostingCode` | Edm.String | Yes | Costing Code | Norma de reparto (dimensión 1) |
| 27 | `CostingCode2` | Edm.String | Yes | Costing Code 2 | Norma de reparto (dimensión 2) |
| 28 | `CostingCode3` | Edm.String | Yes | Costing Code 3 | Norma de reparto (dimensión 3) |
| 29 | `CostingCode4` | Edm.String | Yes | Costing Code 4 | Norma de reparto (dimensión 4) |
| 30 | `CostingCode5` | Edm.String | Yes | Costing Code 5 | Norma de reparto (dimensión 5) |
| 31 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 32 | `LineStatus` | [CountingLineStatusEnum](../Enums/CountingLineStatusEnum.md) | Yes | Line Status | Estado de línea |
| 33 | `CounterType` | [CounterTypeEnum](../Enums/CounterTypeEnum.md) | Yes | Counter Type | Tipo de contador |
| 34 | `CounterID` | Edm.Int32 | Yes | Counter ID | ID del contador |
| 35 | `MultipleCounterRole` | [MultipleCounterRoleEnum](../Enums/MultipleCounterRoleEnum.md) | Yes | Multiple Counter Role | Rol de contador múltiple |
| 36 | `WeightOfRecycledPlastic` | Edm.Double | Yes | Weight Of Recycled Plastic | Peso de plástico reciclado |
| 37 | `PlasticPackageExemptionReason` | Edm.String | Yes | Plastic Package Exemption Reason | Motivo de exención de envases plásticos |
| 38 | `InventoryCountingLineUoMs` | Collection([InventoryCountingLineUoM](../Tipos-Complejos/InventoryCountingLineUoM.md)) | Yes | Inventory Counting Line Uo Ms | Unidades de medida de líneas del recuento |
| 39 | `InventoryCountingSerialNumbers` | Collection([InventoryCountingSerialNumber](../Tipos-Complejos/InventoryCountingSerialNumber.md)) | Yes | Inventory Counting Serial Numbers | Números de serie del recuento de inventario |
| 40 | `InventoryCountingBatchNumbers` | Collection([InventoryCountingBatchNumber](../Tipos-Complejos/InventoryCountingBatchNumber.md)) | Yes | Inventory Counting Batch Numbers | Números de lote del recuento de inventario |

## Used by (properties)

- [InventoryCounting](../Entidades/InventoryCountings.md).`InventoryCountingLines`
