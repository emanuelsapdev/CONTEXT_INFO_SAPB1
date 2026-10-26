# StockTransferLine — Líneas de la transferencia de stock

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `StockTransferLine`
- **Descripción (ES):** Líneas de la transferencia de stock
- **Description (EN):** Stock Transfer Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 45

## Properties (45)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineNum` | Edm.Int32 | Yes | Line Number | Número de línea |
| 2 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 3 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |
| 4 | `ItemDescription` | Edm.String | Yes | Item Description | Descripción del artículo |
| 5 | `Quantity` | Edm.Double | Yes | Quantity | Cantidad |
| 6 | `Price` | Edm.Double | Yes | Price | Precio |
| 7 | `Currency` | Edm.String | Yes | Currency | Moneda |
| 8 | `Rate` | Edm.Double | Yes | Rate | Tasa / tipo de cambio |
| 9 | `DiscountPercent` | Edm.Double | Yes | Discount Percent | Porcentaje de descuento |
| 10 | `VendorNum` | Edm.String | Yes | Vendor Number | Número de proveedor |
| 11 | `SerialNumber` | Edm.String | Yes | Serial Number | Número de serie |
| 12 | `WarehouseCode` | Edm.String | Yes | Warehouse Code | Código de almacén |
| 13 | `FromWarehouseCode` | Edm.String | Yes | From Warehouse Code | Código de almacén de origen |
| 14 | `ProjectCode` | Edm.String | Yes | Project Code | Código de proyecto |
| 15 | `Factor` | Edm.Double | Yes | Factor | Factor |
| 16 | `Factor2` | Edm.Double | Yes | Factor 2 | Factor 2 |
| 17 | `Factor3` | Edm.Double | Yes | Factor 3 | Factor 3 |
| 18 | `Factor4` | Edm.Double | Yes | Factor 4 | Factor 4 |
| 19 | `DistributionRule` | Edm.String | Yes | Distribution Rule | Norma de reparto |
| 20 | `DistributionRule2` | Edm.String | Yes | Distribution Rule 2 | Norma de reparto 2 |
| 21 | `DistributionRule3` | Edm.String | Yes | Distribution Rule 3 | Norma de reparto 3 |
| 22 | `DistributionRule4` | Edm.String | Yes | Distribution Rule 4 | Norma de reparto 4 |
| 23 | `DistributionRule5` | Edm.String | Yes | Distribution Rule 5 | Norma de reparto 5 |
| 24 | `UseBaseUnits` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Use Base Units | Usar unidades base |
| 25 | `MeasureUnit` | Edm.String | Yes | Measure Unit | Unidad de medida |
| 26 | `UnitsOfMeasurment` | Edm.Double | Yes | Units Of Measurment | Unidades de medida |
| 27 | `BaseType` | [InvBaseDocTypeEnum](../Enums/InvBaseDocTypeEnum.md) | Yes | Base Type | Tipo base (tipo de objeto del documento base) |
| 28 | `BaseLine` | Edm.Int32 | Yes | Base Line | Línea base (LineNum del documento base) |
| 29 | `BaseEntry` | Edm.Int32 | Yes | Base Entry | Entrada base (DocEntry del documento base) |
| 30 | `UnitPrice` | Edm.Double | Yes | Unit Price | Precio unitario |
| 31 | `UoMEntry` | Edm.Int32 | Yes | Uo M Entry | Entrada de unidad de medida (UomEntry) |
| 32 | `UoMCode` | Edm.String | Yes | Uo M Code | Código de unidad de medida |
| 33 | `InventoryQuantity` | Edm.Double | Yes | Inventory Quantity | Cantidad de inventario |
| 34 | `RemainingOpenQuantity` | Edm.Double | Yes | Remaining Open Quantity | Cantidad abierta restante |
| 35 | `RemainingOpenInventoryQuantity` | Edm.Double | Yes | Remaining Open Inventory Quantity | Cantidad de inventario abierta restante |
| 36 | `LineStatus` | [BoStatus](../Enums/BoStatus.md) | Yes | Line Status | Estado de línea |
| 37 | `VatGroup` | Edm.String | Yes | Vat Group | Grupo de IVA (indicador de impuesto) |
| 38 | `AdditionalIdentifier` | Edm.String | Yes | Additional Identifier | Identificador adicional |
| 39 | `WeightOfRecycledPlastic` | Edm.Double | Yes | Weight Of Recycled Plastic | Peso de plástico reciclado |
| 40 | `PlasticPackageExemptionReason` | Edm.String | Yes | Plastic Package Exemption Reason | Motivo de exención de envases plásticos |
| 41 | `SerialNumbers` | Collection([SerialNumber](../Tipos-Complejos/SerialNumber.md)) | Yes | Serial Numbers | Números de serie |
| 42 | `BatchNumbers` | Collection([BatchNumber](../Tipos-Complejos/BatchNumber.md)) | Yes | Batch Numbers | Números de lote |
| 43 | `CCDNumbers` | Collection([CCDNumber](../Tipos-Complejos/CCDNumber.md)) | Yes | CCD Numbers | Números de declaración aduanera de carga |
| 44 | `StockTransferLinesBinAllocations` | Collection([StockTransferLinesBinAllocation](../Tipos-Complejos/StockTransferLinesBinAllocation.md)) | Yes | Stock Transfer Lines Bin Allocations | Asignaciones de ubicaciones de las líneas de transferencia |
| 45 | `DocLinePickLists` | Collection([DocLinePickList](../Tipos-Complejos/DocLinePickList.md)) | Yes | Document Line Pick Lists | Listas de picking de la línea del documento |

## Used by (properties)

- [StockTransfer](../Entidades/StockTransfers.md).`StockTransferLines`
