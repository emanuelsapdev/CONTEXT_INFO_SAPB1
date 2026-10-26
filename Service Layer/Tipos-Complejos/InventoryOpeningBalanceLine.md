# InventoryOpeningBalanceLine — Líneas del saldo inicial de inventario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `InventoryOpeningBalanceLine`
- **Descripción (ES):** Líneas del saldo inicial de inventario
- **Description (EN):** Inventory Opening Balance Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 33

## Properties (33)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocumentEntry` | Edm.Int32 | Yes | Document Entry | Entrada del documento |
| 2 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |
| 4 | `ItemDescription` | Edm.String | Yes | Item Description | Descripción del artículo |
| 5 | `WarehouseCode` | Edm.String | Yes | Warehouse Code | Código de almacén |
| 6 | `BinEntry` | Edm.Int32 | Yes | Bin Entry | Entrada de ubicación |
| 7 | `InWarehouseQuantity` | Edm.Double | Yes | In Warehouse Quantity | Cantidad en almacén |
| 8 | `OpeningBalance` | Edm.Double | Yes | Opening Balance | Saldo inicial |
| 9 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 10 | `BarCode` | Edm.String | Yes | Bar Code | Código de barras |
| 11 | `VisualOrder` | Edm.Int32 | Yes | Visual Order | Orden visual |
| 12 | `Price` | Edm.Double | Yes | Price | Precio |
| 13 | `Total` | Edm.Double | Yes | Total | Total |
| 14 | `OpenInventoryAccount` | Edm.String | Yes | Open Inventory Account | Cuenta de inventario inicial |
| 15 | `ProjectCode` | Edm.String | Yes | Project Code | Código de proyecto |
| 16 | `Manufacturer` | Edm.Int32 | Yes | Manufacturer | Fabricante |
| 17 | `SupplierCatalogNo` | Edm.String | Yes | Supplier Catalog Number | N.º de catálogo del proveedor |
| 18 | `CostingCode` | Edm.String | Yes | Costing Code | Norma de reparto (dimensión 1) |
| 19 | `CostingCode2` | Edm.String | Yes | Costing Code 2 | Norma de reparto (dimensión 2) |
| 20 | `CostingCode3` | Edm.String | Yes | Costing Code 3 | Norma de reparto (dimensión 3) |
| 21 | `CostingCode4` | Edm.String | Yes | Costing Code 4 | Norma de reparto (dimensión 4) |
| 22 | `CostingCode5` | Edm.String | Yes | Costing Code 5 | Norma de reparto (dimensión 5) |
| 23 | `PreferredVendor` | Edm.String | Yes | Preferred Vendor | Proveedor preferido |
| 24 | `Currency` | Edm.String | Yes | Currency | Moneda |
| 25 | `AllowBinNegativeQuantity` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Allow Bin Negative Quantity | Permitir cantidad negativa en ubicación |
| 26 | `ActualPrice` | Edm.Double | Yes | Actual Price | Precio real |
| 27 | `PostedValueLC` | Edm.Double | Yes | Posted Value LC (local currency) | Valor contabilizado (moneda local) |
| 28 | `PostedValueSC` | Edm.Double | Yes | Posted Value SC (system currency) | Valor contabilizado (moneda del sistema) |
| 29 | `WeightOfRecycledPlastic` | Edm.Double | Yes | Weight Of Recycled Plastic | Peso de plástico reciclado |
| 30 | `PlasticPackageExemptionReason` | Edm.String | Yes | Plastic Package Exemption Reason | Motivo de exención de envases plásticos |
| 31 | `InventoryOpeningBalanceSerialNumbers` | Collection([InventoryOpeningBalanceSerialNumber](../Tipos-Complejos/InventoryOpeningBalanceSerialNumber.md)) | Yes | Inventory Opening Balance Serial Numbers | Números de serie del saldo inicial de inventario |
| 32 | `InventoryOpeningBalanceBatchNumbers` | Collection([InventoryOpeningBalanceBatchNumber](../Tipos-Complejos/InventoryOpeningBalanceBatchNumber.md)) | Yes | Inventory Opening Balance Batch Numbers | Números de lote del saldo inicial de inventario |
| 33 | `InventoryOpeningBalanceCCDNumbers` | Collection([InventoryOpeningBalanceCCDNumber](../Tipos-Complejos/InventoryOpeningBalanceCCDNumber.md)) | Yes | Inventory Opening Balance CCD Numbers | Números de declaración aduanera del saldo inicial |

## Used by (properties)

- [InventoryOpeningBalance](../Entidades/InventoryOpeningBalances.md).`InventoryOpeningBalanceLines`
