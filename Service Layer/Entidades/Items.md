# Items — Artículos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `Items`
- **Descripción (ES):** Artículos
- **Entity type:** `Item` (open type: accepts dynamic/UDF properties)
- **Key:** `ItemCode` (Edm.String)
- **DB tables (main / lines):** [OITM](../../Tablas%20SAP%20B1/OITM.md), [OITW](../../Tablas%20SAP%20B1/OITW.md), [ITM1](../../Tablas%20SAP%20B1/ITM1.md)
- **ETag / optimistic concurrency:** Yes (`DataVersion`) — send `If-Match` on PATCH/DELETE/actions

- **Properties:** 292 · **Navigation properties:** 44 · **Bound actions:** 1

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/Items?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/Items/$count` | Contar |
| Get by key | `GET /b1s/v2/Items('value')` | Obtener por clave |
| Create | `POST /b1s/v2/Items` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/Items('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/Items('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/Items('value')` (only if the B1 object allows removal) | Borrar |
| Action `Cancel` | `POST /b1s/v2/Items('value')/Cancel` | Cancelar |

## Properties (292)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ItemCode` 🔑 | Edm.String | No | Item Code | Código de artículo |
| 2 | `ItemName` | Edm.String | Yes | Item Name | Nombre del artículo |
| 3 | `ForeignName` | Edm.String | Yes | Foreign Name | Nombre extranjero |
| 4 | `ItemsGroupCode` | Edm.Int32 | Yes | Items Group Code | Código de grupo de artículos |
| 5 | `CustomsGroupCode` | Edm.Int32 | Yes | Customs Group Code | Código de grupo aduanero |
| 6 | `SalesVATGroup` | Edm.String | Yes | Sales VAT Group | Grupo de IVA de ventas |
| 7 | `BarCode` | Edm.String | Yes | Bar Code | Código de barras |
| 8 | `VatLiable` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Vat Liable | Sujeto a IVA |
| 9 | `PurchaseItem` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Purchase Item | Artículo de compra |
| 10 | `SalesItem` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Sales Item | Artículo de venta |
| 11 | `InventoryItem` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Inventory Item | Artículo de inventario |
| 12 | `IncomeAccount` | Edm.String | Yes | Income Account | Cuenta de ingresos |
| 13 | `ExemptIncomeAccount` | Edm.String | Yes | Exempt Income Account | Cuenta de ingresos exentos |
| 14 | `ExpanseAccount` | Edm.String | Yes | Expanse Account | Cuenta de gastos |
| 15 | `Mainsupplier` | Edm.String | Yes | Mainsupplier | Proveedor principal (preferido) |
| 16 | `SupplierCatalogNo` | Edm.String | Yes | Supplier Catalog Number | N.º de catálogo del proveedor |
| 17 | `DesiredInventory` | Edm.Double | Yes | Desired Inventory | Inventario deseado |
| 18 | `MinInventory` | Edm.Double | Yes | Min Inventory | Inventario mínimo |
| 19 | `Picture` | Edm.String | Yes | Picture | Imagen |
| 20 | `User_Text` | Edm.String | Yes | User Text | Texto de usuario |
| 21 | `SerialNum` | Edm.String | Yes | Serial Number | Número de serie |
| 22 | `CommissionPercent` | Edm.Double | Yes | Commission Percent | Porcentaje de comisión |
| 23 | `CommissionSum` | Edm.Double | Yes | Commission Sum | Importe de la comisión |
| 24 | `CommissionGroup` | Edm.Int32 | Yes | Commission Group | Grupo de comisiones |
| 25 | `TreeType` | [BoItemTreeTypes](../Enums/BoItemTreeTypes.md) | Yes | Tree Type | Tipo de árbol (lista de materiales) |
| 26 | `AssetItem` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Asset Item | Artículo de activo |
| 27 | `DataExportCode` | Edm.String | Yes | Data Export Code | Código de exportación de datos |
| 28 | `Manufacturer` | Edm.Int32 | Yes | Manufacturer | Fabricante |
| 29 | `QuantityOnStock` | Edm.Double | Yes | Quantity On Stock | Cantidad en stock |
| 30 | `QuantityOrderedFromVendors` | Edm.Double | Yes | Quantity Ordered From Vendors | Cantidad pedida a proveedores |
| 31 | `QuantityOrderedByCustomers` | Edm.Double | Yes | Quantity Ordered By Customers | Cantidad comprometida por clientes |
| 32 | `ManageSerialNumbers` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Manage Serial Numbers | Gestionar números de serie |
| 33 | `ManageBatchNumbers` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Manage Batch Numbers | Gestionar números de lote |
| 34 | `Valid` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Valid | Válido (activo) |
| 35 | `ValidFrom` | Edm.DateTimeOffset | Yes | Valid From | Válido desde |
| 36 | `ValidTo` | Edm.DateTimeOffset | Yes | Valid To | Válido hasta |
| 37 | `ValidRemarks` | Edm.String | Yes | Valid Remarks | Comentarios de validez |
| 38 | `Frozen` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Frozen | Congelado (inactivo) |
| 39 | `FrozenFrom` | Edm.DateTimeOffset | Yes | Frozen From | Congelado desde |
| 40 | `FrozenTo` | Edm.DateTimeOffset | Yes | Frozen To | Congelado hasta |
| 41 | `FrozenRemarks` | Edm.String | Yes | Frozen Remarks | Comentarios de congelación |
| 42 | `SalesUnit` | Edm.String | Yes | Sales Unit | Unidad de venta |
| 43 | `SalesItemsPerUnit` | Edm.Double | Yes | Sales Items Per Unit | Artículos por unidad de venta |
| 44 | `SalesPackagingUnit` | Edm.String | Yes | Sales Packaging Unit | Unidad de embalaje de venta |
| 45 | `SalesQtyPerPackUnit` | Edm.Double | Yes | Sales Quantity Per Pack Unit | Cantidad por unidad de embalaje de venta |
| 46 | `SalesUnitLength` | Edm.Double | Yes | Sales Unit Length | Longitud de la unidad de venta |
| 47 | `SalesLengthUnit` | Edm.Int32 | Yes | Sales Length Unit | Unidad de longitud de venta |
| 48 | `SalesUnitWidth` | Edm.Double | Yes | Sales Unit Width | Ancho de la unidad de venta |
| 49 | `SalesWidthUnit` | Edm.Int32 | Yes | Sales Width Unit | Unidad de ancho de venta |
| 50 | `SalesUnitHeight` | Edm.Double | Yes | Sales Unit Height | Altura de la unidad de venta |
| 51 | `SalesHeightUnit` | Edm.Int32 | Yes | Sales Height Unit | Unidad de altura de venta |
| 52 | `SalesUnitVolume` | Edm.Double | Yes | Sales Unit Volume | Volumen de la unidad de venta |
| 53 | `SalesVolumeUnit` | Edm.Int32 | Yes | Sales Volume Unit | Unidad de volumen de venta |
| 54 | `SalesUnitWeight` | Edm.Double | Yes | Sales Unit Weight | Peso de la unidad de venta |
| 55 | `SalesWeightUnit` | Edm.Int32 | Yes | Sales Weight Unit | Unidad de peso de venta |
| 56 | `PurchaseUnit` | Edm.String | Yes | Purchase Unit | Unidad de compra |
| 57 | `PurchaseItemsPerUnit` | Edm.Double | Yes | Purchase Items Per Unit | Artículos por unidad de compra |
| 58 | `PurchasePackagingUnit` | Edm.String | Yes | Purchase Packaging Unit | Unidad de embalaje de compra |
| 59 | `PurchaseQtyPerPackUnit` | Edm.Double | Yes | Purchase Quantity Per Pack Unit | Cantidad por unidad de embalaje de compra |
| 60 | `PurchaseUnitLength` | Edm.Double | Yes | Purchase Unit Length | Longitud de la unidad de compra |
| 61 | `PurchaseLengthUnit` | Edm.Int32 | Yes | Purchase Length Unit | Unidad de longitud de compra |
| 62 | `PurchaseUnitWidth` | Edm.Double | Yes | Purchase Unit Width | Ancho de la unidad de compra |
| 63 | `PurchaseWidthUnit` | Edm.Int32 | Yes | Purchase Width Unit | Unidad de ancho de compra |
| 64 | `PurchaseUnitHeight` | Edm.Double | Yes | Purchase Unit Height | Altura de la unidad de compra |
| 65 | `PurchaseHeightUnit` | Edm.Int32 | Yes | Purchase Height Unit | Unidad de altura de compra |
| 66 | `PurchaseUnitVolume` | Edm.Double | Yes | Purchase Unit Volume | Volumen de la unidad de compra |
| 67 | `PurchaseVolumeUnit` | Edm.Int32 | Yes | Purchase Volume Unit | Unidad de volumen de compra |
| 68 | `PurchaseUnitWeight` | Edm.Double | Yes | Purchase Unit Weight | Peso de la unidad de compra |
| 69 | `PurchaseWeightUnit` | Edm.Int32 | Yes | Purchase Weight Unit | Unidad de peso de compra |
| 70 | `PurchaseVATGroup` | Edm.String | Yes | Purchase VAT Group | Grupo de IVA de compras |
| 71 | `SalesFactor1` | Edm.Double | Yes | Sales Factor 1 | Factor de venta 1 |
| 72 | `SalesFactor2` | Edm.Double | Yes | Sales Factor 2 | Factor de venta 2 |
| 73 | `SalesFactor3` | Edm.Double | Yes | Sales Factor 3 | Factor de venta 3 |
| 74 | `SalesFactor4` | Edm.Double | Yes | Sales Factor 4 | Factor de venta 4 |
| 75 | `PurchaseFactor1` | Edm.Double | Yes | Purchase Factor 1 | Factor de compra 1 |
| 76 | `PurchaseFactor2` | Edm.Double | Yes | Purchase Factor 2 | Factor de compra 2 |
| 77 | `PurchaseFactor3` | Edm.Double | Yes | Purchase Factor 3 | Factor de compra 3 |
| 78 | `PurchaseFactor4` | Edm.Double | Yes | Purchase Factor 4 | Factor de compra 4 |
| 79 | `MovingAveragePrice` | Edm.Double | Yes | Moving Average Price | Precio promedio ponderado |
| 80 | `ForeignRevenuesAccount` | Edm.String | Yes | Foreign Revenues Account | Cuenta de ingresos del exterior |
| 81 | `ECRevenuesAccount` | Edm.String | Yes | EC Revenues Account | Cuenta de ingresos CE |
| 82 | `ForeignExpensesAccount` | Edm.String | Yes | Foreign Expenses Account | Cuenta de gastos del exterior |
| 83 | `ECExpensesAccount` | Edm.String | Yes | EC Expenses Account | Cuenta de gastos CE |
| 84 | `AvgStdPrice` | Edm.Double | Yes | Avg Std Price | Precio promedio/estándar |
| 85 | `DefaultWarehouse` | Edm.String | Yes | Default Warehouse | Almacén predeterminado |
| 86 | `ShipType` | Edm.Int32 | Yes | Ship Type | Clase de expedición |
| 87 | `GLMethod` | [BoGLMethods](../Enums/BoGLMethods.md) | Yes | G/L Method | Método de cuentas de mayor (por almacén/grupo/artículo) |
| 88 | `TaxType` | [BoTaxTypes](../Enums/BoTaxTypes.md) | Yes | Tax Type | Tipo de impuesto |
| 89 | `MaxInventory` | Edm.Double | Yes | Max Inventory | Inventario máximo |
| 90 | `ManageStockByWarehouse` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Manage Stock By Warehouse | Gestionar stock por almacén |
| 91 | `PurchaseHeightUnit1` | Edm.Int32 | Yes | Purchase Height Unit 1 | Unidad de altura de compra 1 |
| 92 | `PurchaseUnitHeight1` | Edm.Double | Yes | Purchase Unit Height 1 | Altura de la unidad de compra 1 |
| 93 | `PurchaseLengthUnit1` | Edm.Int32 | Yes | Purchase Length Unit 1 | Unidad de longitud de compra 1 |
| 94 | `PurchaseUnitLength1` | Edm.Double | Yes | Purchase Unit Length 1 | Longitud de la unidad de compra 1 |
| 95 | `PurchaseWeightUnit1` | Edm.Int32 | Yes | Purchase Weight Unit 1 | Unidad de peso de compra 1 |
| 96 | `PurchaseUnitWeight1` | Edm.Double | Yes | Purchase Unit Weight 1 | Peso de la unidad de compra 1 |
| 97 | `PurchaseWidthUnit1` | Edm.Int32 | Yes | Purchase Width Unit 1 | Unidad de ancho de compra 1 |
| 98 | `PurchaseUnitWidth1` | Edm.Double | Yes | Purchase Unit Width 1 | Ancho de la unidad de compra 1 |
| 99 | `SalesHeightUnit1` | Edm.Int32 | Yes | Sales Height Unit 1 | Unidad de altura de venta 1 |
| 100 | `SalesUnitHeight1` | Edm.Double | Yes | Sales Unit Height 1 | Altura de la unidad de venta 1 |
| 101 | `SalesLengthUnit1` | Edm.Int32 | Yes | Sales Length Unit 1 | Unidad de longitud de venta 1 |
| 102 | `SalesUnitLength1` | Edm.Double | Yes | Sales Unit Length 1 | Longitud de la unidad de venta 1 |
| 103 | `SalesWeightUnit1` | Edm.Int32 | Yes | Sales Weight Unit 1 | Unidad de peso de venta 1 |
| 104 | `SalesUnitWeight1` | Edm.Double | Yes | Sales Unit Weight 1 | Peso de la unidad de venta 1 |
| 105 | `SalesWidthUnit1` | Edm.Int32 | Yes | Sales Width Unit 1 | Unidad de ancho de venta 1 |
| 106 | `SalesUnitWidth1` | Edm.Double | Yes | Sales Unit Width 1 | Ancho de la unidad de venta 1 |
| 107 | `ForceSelectionOfSerialNumber` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Force Selection Of Serial Number | Forzar selección de número de serie |
| 108 | `ManageSerialNumbersOnReleaseOnly` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Manage Serial Numbers On Release Only | Gestionar números de serie solo al liberar |
| 109 | `WTLiable` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Withholding Tax Liable | Sujeto a retención |
| 110 | `CostAccountingMethod` | [BoInventorySystem](../Enums/BoInventorySystem.md) | Yes | Cost Accounting Method | Método de contabilidad de costos |
| 111 | `SWW` | Edm.String | Yes | SWW | SWW (código de servicio) |
| 112 | `WarrantyTemplate` | Edm.String | Yes | Warranty Template | Plantilla de garantía |
| 113 | `IndirectTax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Indirect Tax | Impuesto indirecto |
| 114 | `ArTaxCode` | Edm.String | Yes | Ar Tax Code | Indicador de impuesto (ventas) |
| 115 | `ApTaxCode` | Edm.String | Yes | Ap Tax Code | Indicador de impuesto (compras) |
| 116 | `BaseUnitName` | Edm.String | Yes | Base Unit Name | Nombre de la unidad base |
| 117 | `ItemCountryOrg` | Edm.String | Yes | Item Country Org | País de origen del artículo |
| 118 | `IssueMethod` | [BoIssueMethod](../Enums/BoIssueMethod.md) | Yes | Issue Method | Método de emisión (manual/notificación) |
| 119 | `SRIAndBatchManageMethod` | [BoManageMethod](../Enums/BoManageMethod.md) | Yes | SRI And Batch Manage Method | Método de gestión de series y lotes |
| 120 | `IsPhantom` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Phantom | Es fantasma |
| 121 | `InventoryUOM` | Edm.String | Yes | Inventory Unit of Measure | Unidad de medida de inventario |
| 122 | `PlanningSystem` | [BoPlanningSystem](../Enums/BoPlanningSystem.md) | Yes | Planning System | Sistema de planificación (MRP/ninguno) |
| 123 | `ProcurementMethod` | [BoProcurementMethod](../Enums/BoProcurementMethod.md) | Yes | Procurement Method | Método de aprovisionamiento (comprar/fabricar) |
| 124 | `ComponentWarehouse` | [BoMRPComponentWarehouse](../Enums/BoMRPComponentWarehouse.md) | Yes | Component Warehouse | Almacén de componentes |
| 125 | `OrderIntervals` | Edm.Int32 | Yes | Order Intervals | Intervalos de pedidos |
| 126 | `OrderMultiple` | Edm.Double | Yes | Order Multiple | Múltiplo de pedido |
| 127 | `LeadTime` | Edm.Int32 | Yes | Lead Time | Tiempo de entrega |
| 128 | `MinOrderQuantity` | Edm.Double | Yes | Min Order Quantity | Cantidad mínima de pedido |
| 129 | `ItemType` | [ItemTypeEnum](../Enums/ItemTypeEnum.md) | Yes | Item Type | Tipo de artículo |
| 130 | `ItemClass` | [ItemClassEnum](../Enums/ItemClassEnum.md) | Yes | Item Class | Clase de artículo (material/servicio) |
| 131 | `OutgoingServiceCode` | Edm.Int32 | Yes | Outgoing Service Code | Código de servicio saliente |
| 132 | `IncomingServiceCode` | Edm.Int32 | Yes | Incoming Service Code | Código de servicio entrante |
| 133 | `ServiceGroup` | Edm.Int32 | Yes | Service Group | Grupo de servicios |
| 134 | `NCMCode` | Edm.Int32 | Yes | NCM Code | Código NCM |
| 135 | `MaterialType` | [BoMaterialTypes](../Enums/BoMaterialTypes.md) | Yes | Material Type | Tipo de material |
| 136 | `MaterialGroup` | Edm.Int32 | Yes | Material Group | Grupo de materiales |
| 137 | `ProductSource` | Edm.String | Yes | Product Source | Origen del producto |
| 138 | `Properties1` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 1 | Propiedad 1 |
| 139 | `Properties2` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 2 | Propiedad 2 |
| 140 | `Properties3` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 3 | Propiedad 3 |
| 141 | `Properties4` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 4 | Propiedad 4 |
| 142 | `Properties5` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 5 | Propiedad 5 |
| 143 | `Properties6` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 6 | Propiedad 6 |
| 144 | `Properties7` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 7 | Propiedad 7 |
| 145 | `Properties8` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 8 | Propiedad 8 |
| 146 | `Properties9` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 9 | Propiedad 9 |
| 147 | `Properties10` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 10 | Propiedad 10 |
| 148 | `Properties11` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 11 | Propiedad 11 |
| 149 | `Properties12` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 12 | Propiedad 12 |
| 150 | `Properties13` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 13 | Propiedad 13 |
| 151 | `Properties14` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 14 | Propiedad 14 |
| 152 | `Properties15` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 15 | Propiedad 15 |
| 153 | `Properties16` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 16 | Propiedad 16 |
| 154 | `Properties17` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 17 | Propiedad 17 |
| 155 | `Properties18` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 18 | Propiedad 18 |
| 156 | `Properties19` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 19 | Propiedad 19 |
| 157 | `Properties20` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 20 | Propiedad 20 |
| 158 | `Properties21` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 21 | Propiedad 21 |
| 159 | `Properties22` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 22 | Propiedad 22 |
| 160 | `Properties23` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 23 | Propiedad 23 |
| 161 | `Properties24` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 24 | Propiedad 24 |
| 162 | `Properties25` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 25 | Propiedad 25 |
| 163 | `Properties26` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 26 | Propiedad 26 |
| 164 | `Properties27` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 27 | Propiedad 27 |
| 165 | `Properties28` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 28 | Propiedad 28 |
| 166 | `Properties29` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 29 | Propiedad 29 |
| 167 | `Properties30` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 30 | Propiedad 30 |
| 168 | `Properties31` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 31 | Propiedad 31 |
| 169 | `Properties32` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 32 | Propiedad 32 |
| 170 | `Properties33` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 33 | Propiedad 33 |
| 171 | `Properties34` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 34 | Propiedad 34 |
| 172 | `Properties35` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 35 | Propiedad 35 |
| 173 | `Properties36` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 36 | Propiedad 36 |
| 174 | `Properties37` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 37 | Propiedad 37 |
| 175 | `Properties38` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 38 | Propiedad 38 |
| 176 | `Properties39` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 39 | Propiedad 39 |
| 177 | `Properties40` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 40 | Propiedad 40 |
| 178 | `Properties41` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 41 | Propiedad 41 |
| 179 | `Properties42` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 42 | Propiedad 42 |
| 180 | `Properties43` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 43 | Propiedad 43 |
| 181 | `Properties44` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 44 | Propiedad 44 |
| 182 | `Properties45` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 45 | Propiedad 45 |
| 183 | `Properties46` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 46 | Propiedad 46 |
| 184 | `Properties47` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 47 | Propiedad 47 |
| 185 | `Properties48` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 48 | Propiedad 48 |
| 186 | `Properties49` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 49 | Propiedad 49 |
| 187 | `Properties50` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 50 | Propiedad 50 |
| 188 | `Properties51` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 51 | Propiedad 51 |
| 189 | `Properties52` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 52 | Propiedad 52 |
| 190 | `Properties53` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 53 | Propiedad 53 |
| 191 | `Properties54` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 54 | Propiedad 54 |
| 192 | `Properties55` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 55 | Propiedad 55 |
| 193 | `Properties56` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 56 | Propiedad 56 |
| 194 | `Properties57` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 57 | Propiedad 57 |
| 195 | `Properties58` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 58 | Propiedad 58 |
| 196 | `Properties59` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 59 | Propiedad 59 |
| 197 | `Properties60` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 60 | Propiedad 60 |
| 198 | `Properties61` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 61 | Propiedad 61 |
| 199 | `Properties62` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 62 | Propiedad 62 |
| 200 | `Properties63` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 63 | Propiedad 63 |
| 201 | `Properties64` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Properties 64 | Propiedad 64 |
| 202 | `AutoCreateSerialNumbersOnRelease` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Auto Create Serial Numbers On Release | Crear números de serie automáticamente al liberar |
| 203 | `DNFEntry` | Edm.Int32 | Yes | DNF Entry | Entrada DNF |
| 204 | `GTSItemSpec` | Edm.String | Yes | GTS Item Spec | Especificación de artículo GTS |
| 205 | `GTSItemTaxCategory` | Edm.String | Yes | GTS Item Tax Category | Categoría de impuesto de artículo GTS |
| 206 | `FuelID` | Edm.Int32 | Yes | Fuel ID | ID de combustible |
| 207 | `BeverageTableCode` | Edm.String | Yes | Beverage Table Code | Código de tabla de bebida |
| 208 | `BeverageGroupCode` | Edm.String | Yes | Beverage Group Code | Código de grupo de bebida |
| 209 | `BeverageCommercialBrandCode` | Edm.Int32 | Yes | Beverage Commercial Brand Code | Código de marca comercial de bebida |
| 210 | `Series` | Edm.Int32 | Yes | Series | Serie de numeración |
| 211 | `ToleranceDays` | Edm.Int32 | Yes | Tolerance Days | Días de tolerancia |
| 212 | `TypeOfAdvancedRules` | [TypeOfAdvancedRulesEnum](../Enums/TypeOfAdvancedRulesEnum.md) | Yes | Type Of Advanced Rules | Tipo de reglas avanzadas |
| 213 | `IssuePrimarilyBy` | [IssuePrimarilyByEnum](../Enums/IssuePrimarilyByEnum.md) | Yes | Issue Primarily By | Emitir principalmente por |
| 214 | `NoDiscounts` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Number Discounts | Sin descuentos |
| 215 | `AssetClass` | Edm.String | Yes | Asset Class | Clase de activo |
| 216 | `AssetGroup` | Edm.String | Yes | Asset Group | Grupo de activos |
| 217 | `InventoryNumber` | Edm.String | Yes | Inventory Number | Número de inventario |
| 218 | `Technician` | Edm.Int32 | Yes | Technician | Técnico |
| 219 | `Employee` | Edm.Int32 | Yes | Employee | Empleado |
| 220 | `Location` | Edm.Int32 | Yes | Location | Ubicación |
| 221 | `AssetStatus` | [AssetStatusEnum](../Enums/AssetStatusEnum.md) | Yes | Asset Status | Estado del activo |
| 222 | `CapitalizationDate` | Edm.DateTimeOffset | Yes | Capitalization Date | Fecha de capitalización |
| 223 | `StatisticalAsset` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Statistical Asset | Activo estadístico |
| 224 | `Cession` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Cession | Cesión |
| 225 | `DeactivateAfterUsefulLife` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Deactivate After Useful Life | Desactivar al finalizar la vida útil |
| 226 | `ManageByQuantity` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Manage By Quantity | Gestionar por cantidad |
| 227 | `UoMGroupEntry` | Edm.Int32 | Yes | Uo M Group Entry | Grupo de unidades de medida |
| 228 | `InventoryUoMEntry` | Edm.Int32 | Yes | Inventory Uo M Entry | Entrada de unidad de medida de inventario |
| 229 | `DefaultSalesUoMEntry` | Edm.Int32 | Yes | Default Sales Uo M Entry | Unidad de medida de venta predeterminada |
| 230 | `DefaultPurchasingUoMEntry` | Edm.Int32 | Yes | Default Purchasing Uo M Entry | Unidad de medida de compra predeterminada |
| 231 | `DepreciationGroup` | Edm.String | Yes | Depreciation Group | Grupo de amortización |
| 232 | `AssetSerialNumber` | Edm.String | Yes | Asset Serial Number | Número de serie del activo |
| 233 | `InventoryWeight` | Edm.Double | Yes | Inventory Weight | Peso de inventario |
| 234 | `InventoryWeightUnit` | Edm.Int32 | Yes | Inventory Weight Unit | Unidad de peso de inventario |
| 235 | `InventoryWeight1` | Edm.Double | Yes | Inventory Weight 1 | Peso de inventario 1 |
| 236 | `InventoryWeightUnit1` | Edm.Int32 | Yes | Inventory Weight Unit 1 | Unidad de peso de inventario 1 |
| 237 | `DefaultCountingUnit` | Edm.String | Yes | Default Counting Unit | Unidad de recuento predeterminada |
| 238 | `CountingItemsPerUnit` | Edm.Double | Yes | Counting Items Per Unit | Artículos por unidad de recuento |
| 239 | `DefaultCountingUoMEntry` | Edm.Int32 | Yes | Default Counting Uo M Entry | Unidad de medida de recuento predeterminada |
| 240 | `Excisable` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Excisable | Sujeto a impuestos especiales |
| 241 | `ChapterID` | Edm.Int32 | Yes | Chapter ID | ID de capítulo |
| 242 | `ScsCode` | Edm.String | Yes | Scs Code | Código SCS |
| 243 | `SpProdType` | [SpecialProductTypeEnum](../Enums/SpecialProductTypeEnum.md) | Yes | Sp Prod Type | Tipo de producción especial |
| 244 | `ProdStdCost` | Edm.Double | Yes | Prod Std Cost | Costo estándar de producción |
| 245 | `InCostRollup` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | In Cost Rollup | En acumulación de costos |
| 246 | `VirtualAssetItem` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Virtual Asset Item | Artículo de activo virtual |
| 247 | `EnforceAssetSerialNumbers` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enforce Asset Serial Numbers | Exigir números de serie de activos |
| 248 | `AttachmentEntry` | Edm.Int32 | Yes | Attachment Entry | Entrada de anexo (ID) |
| 249 | `LinkedResource` | Edm.String | Yes | Linked Resource | Recurso vinculado |
| 250 | `UpdateDate` | Edm.DateTimeOffset | Yes | Update Date | Fecha de actualización |
| 251 | `UpdateTime` | Edm.TimeOfDay | Yes | Update Time | Hora de actualización |
| 252 | `GSTRelevnt` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | GST Relevnt | Relevante para GST |
| 253 | `SACEntry` | Edm.Int32 | Yes | SAC Entry | Entrada SAC |
| 254 | `GSTTaxCategory` | [GSTTaxCategoryEnum](../Enums/GSTTaxCategoryEnum.md) | Yes | GST Tax Category | Categoría de impuesto GST |
| 255 | `ServiceCategoryEntry` | Edm.Int32 | Yes | Service Category Entry | Categoría de servicio |
| 256 | `CapitalGoodsOnHoldPercent` | Edm.Double | Yes | Capital Goods On Hold Percent | Porcentaje de bienes de capital retenidos |
| 257 | `CapitalGoodsOnHoldLimit` | Edm.Double | Yes | Capital Goods On Hold Limit | Límite de bienes de capital retenidos |
| 258 | `AssessableValue` | Edm.Double | Yes | Assessable Value | Valor imponible |
| 259 | `AssVal4WTR` | Edm.Double | Yes | Ass Val 4 WTR | Valor imponible para transferencia de stock |
| 260 | `SOIExcisable` | [SOIExcisableTypeEnum](../Enums/SOIExcisableTypeEnum.md) | Yes | SOI Excisable | Sujeto a impuestos especiales (SOI) |
| 261 | `TNVED` | Edm.String | Yes | TNVED | Código TN VED (Rusia) |
| 262 | `ImportedItem` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Imported Item | Artículo importado |
| 263 | `PricingUnit` | Edm.Int32 | Yes | Pricing Unit | Unidad de fijación de precios |
| 264 | `CreateDate` | Edm.DateTimeOffset | Yes | Create Date | Fecha de creación |
| 265 | `CreateTime` | Edm.TimeOfDay | Yes | Create Time | Hora de creación |
| 266 | `NVECode` | Edm.String | Yes | NVE Code | Código NVE |
| 267 | `CtrSealQty` | Edm.Double | Yes | Ctr Seal Quantity | Cantidad de precintos del contenedor |
| 268 | `CESTCode` | Edm.Int32 | Yes | CEST Code | Código CEST |
| 269 | `LegalText` | Edm.String | Yes | Legal Text | Texto legal |
| 270 | `DataVersion` | Edm.Int32 | Yes | Data Version | Versión de datos (control de concurrencia) |
| 271 | `CreateQRCodeFrom` | Edm.String | Yes | Create QR Code From | Crear código QR desde |
| 272 | `TraceableItem` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Traceable Item | Artículo trazable |
| 273 | `CommodityClassification` | Edm.Int32 | Yes | Commodity Classification | Clasificación de mercancía |
| 274 | `WeightOfRecycledPlastic` | Edm.Double | Yes | Weight Of Recycled Plastic | Peso de plástico reciclado |
| 275 | `PlasticPackageTaxCategory` | Edm.String | Yes | Plastic Package Tax Category | Categoría de impuesto a envases plásticos |
| 276 | `PlasticPackageExemptionReasonForPurchase` | Edm.String | Yes | Plastic Package Exemption Reason For Purchase | Motivo de exención de envases plásticos (compras) |
| 277 | `PlasticPackageExemptionReasonForProduction` | Edm.String | Yes | Plastic Package Exemption Reason For Production | Motivo de exención de envases plásticos (producción) |
| 278 | `SAFTProductType` | [SAFTProductTypeEnum](../Enums/SAFTProductTypeEnum.md) | Yes | SAFT Product Type | Tipo de producto SAF-T |
| 279 | `SAFTProductTypeEx` | Edm.String | Yes | SAFT Product Type Ex | Tipo de producto SAF-T (ampliado) |
| 280 | `U_B1SYS_MTXCode` | Edm.Int32 | Yes | [AR localization] MTX Code | [Loc. AR] Código de unidad de medida AFIP (MTX) |
| 281 | `ItemPrices` | Collection([ItemPrice](../Tipos-Complejos/ItemPrice.md)) | Yes | Item Prices | Precios del artículo |
| 282 | `ItemWarehouseInfoCollection` | Collection([ItemWarehouseInfo](../Tipos-Complejos/ItemWarehouseInfo.md)) | Yes | Item Warehouse Information Collection | Colección de datos de almacén del artículo |
| 283 | `ItemPreferredVendors` | Collection([ItemPreferredVendor](../Tipos-Complejos/ItemPreferredVendor.md)) | Yes | Item Preferred Vendors | Proveedores preferidos del artículo |
| 284 | `ItemLocalizationInfos` | Collection([ItemLocalizationInfo](../Tipos-Complejos/ItemLocalizationInfo.md)) | Yes | Item Localization Infos | Información de localización del artículo |
| 285 | `ItemProjects` | Collection([ItemProject](../Tipos-Complejos/ItemProject.md)) | Yes | Item Projects | Proyectos del artículo |
| 286 | `ItemDistributionRules` | Collection([ItemDistributionRule](../Tipos-Complejos/ItemDistributionRule.md)) | Yes | Item Distribution Rules | Normas de reparto del artículo |
| 287 | `ItemAttributeGroups` | Collection([ItemAttributeGroups](../Tipos-Complejos/ItemAttributeGroups.md)) | Yes | Item Attribute Groups | Grupos de atributos del artículo |
| 288 | `ItemDepreciationParameters` | Collection([ItemDepreciationParameter](../Tipos-Complejos/ItemDepreciationParameter.md)) | Yes | Item Depreciation Parameters | Parámetros de amortización del artículo |
| 289 | `ItemPeriodControls` | Collection([ItemPeriodControl](../Tipos-Complejos/ItemPeriodControl.md)) | Yes | Item Period Controls | Control de períodos del artículo |
| 290 | `ItemUnitOfMeasurementCollection` | Collection([ItemUnitOfMeasurement](../Tipos-Complejos/ItemUnitOfMeasurement.md)) | Yes | Item Unit Of Measurement Collection | Colección de unidades de medida del artículo |
| 291 | `ItemBarCodeCollection` | Collection([ItemBarCode](../Tipos-Complejos/ItemBarCode.md)) | Yes | Item Bar Code Collection | Colección de códigos de barras del artículo |
| 292 | `ItemIntrastatExtension` | [ItemIntrastatExtension](../Tipos-Complejos/ItemIntrastatExtension.md) | Yes | Item Intrastat Extension | Extensión Intrastat del artículo |

## Navigation properties (44)

Use `GET /b1s/v2/Items('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `ProductTrees` | Collection([ProductTree](../Entidades/ProductTrees.md)) | [ProductTrees](ProductTrees.md) |  | Listas de materiales (árbol de producto) |
| `CustomerEquipmentCards` | Collection([CustomerEquipmentCard](../Entidades/CustomerEquipmentCards.md)) | [CustomerEquipmentCards](CustomerEquipmentCards.md) |  | Tarjetas de equipo del cliente |
| `ServiceCalls` | Collection([ServiceCall](../Entidades/ServiceCalls.md)) | [ServiceCalls](ServiceCalls.md) |  | Llamadas de servicio |
| `ItemGroups` | [ItemGroups](../Entidades/ItemGroups.md) | [ItemGroups](ItemGroups.md) | ItemsGroupCode → Number | Grupos de artículos |
| `CustomsGroup` | [CustomsGroup](../Entidades/CustomsGroups.md) | [CustomsGroups](CustomsGroups.md) | CustomsGroupCode → Code | Grupos aduaneros |
| `VatGroup` | [VatGroup](../Entidades/VatGroups.md) | [VatGroups](VatGroups.md) | SalesVATGroup → Code | Grupo de IVA (indicador de impuesto) |
| `ChartOfAccount` | [ChartOfAccount](../Entidades/ChartOfAccounts.md) | [ChartOfAccounts](ChartOfAccounts.md) | IncomeAccount → Code | Plan de cuentas (cuentas de mayor) |
| `BusinessPartner` | [BusinessPartner](../Entidades/BusinessPartners.md) | [BusinessPartners](BusinessPartners.md) | Mainsupplier → CardCode | Socio de negocios |
| `CommissionGroup2` | [CommissionGroup](../Entidades/CommissionGroups.md) | [CommissionGroups](CommissionGroups.md) | CommissionGroup → CommissionGroupCode | Grupos de comisiones |
| `Manufacturer2` | [Manufacturer](../Entidades/Manufacturers.md) | [Manufacturers](Manufacturers.md) | Manufacturer → Code | Fabricantes |
| `ShippingType` | [ShippingType](../Entidades/ShippingTypes.md) | [ShippingTypes](ShippingTypes.md) | ShipType → Code | Clase de expedición |
| `ContractTemplate` | [ContractTemplate](../Entidades/ContractTemplates.md) | [ContractTemplates](ContractTemplates.md) | WarrantyTemplate → TemplateName | Plantilla de contrato |
| `SalesTaxCode` | [SalesTaxCode](../Entidades/SalesTaxCodes.md) | [SalesTaxCodes](SalesTaxCodes.md) | ArTaxCode → Code | Códigos del impuesto sobre ventas |
| `InventoryCycles` | [InventoryCycles](../Entidades/InventoryCycles.md) | [InventoryCycles](InventoryCycles.md) | OrderIntervals → CycleCode | Ciclos de inventario |
| `ServiceGroup2` | [ServiceGroup](../Entidades/ServiceGroups.md) | [ServiceGroups](ServiceGroups.md) | ServiceGroup → AbsEntry | Grupos de servicios |
| `NCMCodeSetup` | [NCMCodeSetup](../Entidades/NCMCodesSetup.md) | [NCMCodesSetup](NCMCodesSetup.md) | NCMCode → AbsEntry | Configuración de códigos NCM |
| `MaterialGroup2` | [MaterialGroup](../Entidades/MaterialGroups.md) | [MaterialGroups](MaterialGroups.md) | MaterialGroup → AbsEntry | Grupos de materiales |
| `DNFCodeSetup` | [DNFCodeSetup](../Entidades/DNFCodeSetup.md) | [DNFCodeSetup](DNFCodeSetup.md) | DNFEntry → AbsEntry | Configuración de códigos DNF |
| `BrazilFuelIndexer` | [BrazilFuelIndexer](../Entidades/BrazilFuelIndexers.md) | [BrazilFuelIndexers](BrazilFuelIndexers.md) | FuelID → FuelID | Brasil - Indexadores de combustibles |
| `BrazilStringIndexer` | [BrazilStringIndexer](../Entidades/BrazilStringIndexers.md) | [BrazilStringIndexers](BrazilStringIndexers.md) | BeverageTableCode → ID | Brasil - Indexadores de cadenas |
| `BrazilNumericIndexer` | [BrazilNumericIndexer](../Entidades/BrazilNumericIndexers.md) | [BrazilNumericIndexers](BrazilNumericIndexers.md) | BeverageCommercialBrandCode → ID | Brasil - Indexadores numéricos |
| `AssetClass2` | [AssetClass](../Entidades/AssetClasses.md) | [AssetClasses](AssetClasses.md) | AssetClass → Code | Clases de activos |
| `AssetGroup2` | [AssetGroup](../Entidades/AssetGroups.md) | [AssetGroups](AssetGroups.md) | AssetGroup → Code | Grupos de activos |
| `EmployeeInfo` | [EmployeeInfo](../Entidades/EmployeesInfo.md) | [EmployeesInfo](EmployeesInfo.md) | Technician → EmployeeID | Empleados |
| `WarehouseLocation` | [WarehouseLocation](../Entidades/WarehouseLocations.md) | [WarehouseLocations](WarehouseLocations.md) | Location → Code | Ubicaciones de almacenes |
| `UnitOfMeasurementGroup` | [UnitOfMeasurementGroup](../Entidades/UnitOfMeasurementGroups.md) | [UnitOfMeasurementGroups](UnitOfMeasurementGroups.md) | UoMGroupEntry → AbsEntry | Grupos de unidades de medida |
| `UnitOfMeasurement` | [UnitOfMeasurement](../Entidades/UnitOfMeasurements.md) | [UnitOfMeasurements](UnitOfMeasurements.md) | InventoryUoMEntry → AbsEntry | Unidades de medida |
| `AssetDepreciationGroup` | [AssetDepreciationGroup](../Entidades/AssetDepreciationGroups.md) | [AssetDepreciationGroups](AssetDepreciationGroups.md) | DepreciationGroup → Code | Grupos de amortización de activos |
| `IndiaHsn` | [IndiaHsn](../Entidades/IndiaHsn.md) | [IndiaHsn](IndiaHsn.md) | ChapterID → AbsEntry | India - Códigos HSN |
| `Resource` | [Resource](../Entidades/Resources.md) | [Resources](Resources.md) | LinkedResource → Code | Recursos |
| `IndiaSacCode` | [IndiaSacCode](../Entidades/IndiaSacCode.md) | [IndiaSacCode](IndiaSacCode.md) | SACEntry → AbsEntry | India - Códigos SAC |
| `CESTCodeData` | [CESTCodeData](../Entidades/CESTCodes.md) | [CESTCodes](CESTCodes.md) | CESTCode → AbsEntry | Códigos CEST |
| `IdentificationCode` | [IdentificationCode](../Entidades/IdentificationCodes.md) | [IdentificationCodes](IdentificationCodes.md) | CommodityClassification → AbsEntry | Códigos de identificación |
| `BinLocations` | Collection([BinLocation](../Entidades/BinLocations.md)) | [BinLocations](BinLocations.md) |  | Ubicaciones (bin locations) |
| `AlternateCatNum` | Collection([AlternateCatNum](../Entidades/AlternateCatNum.md)) | [AlternateCatNum](AlternateCatNum.md) |  | Números de catálogo de socios de negocios |
| `GLAccountAdvancedRules` | Collection([GLAccountAdvancedRule](../Entidades/GLAccountAdvancedRules.md)) | [GLAccountAdvancedRules](GLAccountAdvancedRules.md) |  | Reglas avanzadas de cuentas de mayor |
| `BarCodes` | Collection([BarCode](../Entidades/BarCodes.md)) | [BarCodes](BarCodes.md) |  | Códigos de barras |
| `Resources` | Collection([Resource](../Entidades/Resources.md)) | [Resources](Resources.md) |  | Recursos |
| `KnowledgeBaseSolutions` | Collection([KnowledgeBaseSolution](../Entidades/KnowledgeBaseSolutions.md)) | [KnowledgeBaseSolutions](KnowledgeBaseSolutions.md) |  | Soluciones de la base de conocimiento |
| `DepreciationAreas` | Collection([DepreciationArea](../Entidades/DepreciationAreas.md)) | [DepreciationAreas](DepreciationAreas.md) |  | Áreas de amortización |
| `SpecialPrices` | Collection([SpecialPrice](../Entidades/SpecialPrices.md)) | [SpecialPrices](SpecialPrices.md) |  | Precios especiales |
| `SerialNumberDetails` | Collection([SerialNumberDetail](../Entidades/SerialNumberDetails.md)) | [SerialNumberDetails](SerialNumberDetails.md) |  | Detalles de números de serie |
| `BatchNumberDetails` | Collection([BatchNumberDetail](../Entidades/BatchNumberDetails.md)) | [BatchNumberDetails](BatchNumberDetails.md) |  | Detalles de números de lote |
| `StockTakings` | Collection([StockTaking](../Entidades/StockTakings.md)) | [StockTakings](StockTakings.md) |  | Toma de inventario |

## Bound actions (1)

### Cancel

- **Descripción (ES):** Cancelar
- **Request:** `POST /b1s/v2/Items('value')/Cancel`


## Service operations that use this type

- [`ItemsService_InitData`](../Servicios/ItemsService.md#itemsservice_initdata)
