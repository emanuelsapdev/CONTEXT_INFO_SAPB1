# DocumentLine — Línea del documento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DocumentLine`
- **Descripción (ES):** Línea del documento
- **Description (EN):** Document Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 245

## Properties (245)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineNum` | Edm.Int32 | Yes | Line Number | Número de línea |
| 2 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |
| 3 | `ItemDescription` | Edm.String | Yes | Item Description | Descripción del artículo |
| 4 | `Quantity` | Edm.Double | Yes | Quantity | Cantidad |
| 5 | `ShipDate` | Edm.DateTimeOffset | Yes | Ship Date | Fecha de envío |
| 6 | `Price` | Edm.Double | Yes | Price | Precio |
| 7 | `PriceAfterVAT` | Edm.Double | Yes | Price After VAT | Precio después de IVA (bruto) |
| 8 | `Currency` | Edm.String | Yes | Currency | Moneda |
| 9 | `Rate` | Edm.Double | Yes | Rate | Tasa / tipo de cambio |
| 10 | `DiscountPercent` | Edm.Double | Yes | Discount Percent | Porcentaje de descuento |
| 11 | `VendorNum` | Edm.String | Yes | Vendor Number | Número de proveedor |
| 12 | `SerialNum` | Edm.String | Yes | Serial Number | Número de serie |
| 13 | `WarehouseCode` | Edm.String | Yes | Warehouse Code | Código de almacén |
| 14 | `SalesPersonCode` | Edm.Int32 | Yes | Sales Person Code | Código del empleado de ventas |
| 15 | `CommisionPercent` | Edm.Double | Yes | Commision Percent | Porcentaje de comisión |
| 16 | `TreeType` | [BoItemTreeTypes](../Enums/BoItemTreeTypes.md) | Yes | Tree Type | Tipo de árbol (lista de materiales) |
| 17 | `AccountCode` | Edm.String | Yes | Account Code | Código de cuenta |
| 18 | `UseBaseUnits` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Use Base Units | Usar unidades base |
| 19 | `SupplierCatNum` | Edm.String | Yes | Supplier Category Number | N.º de catálogo del proveedor |
| 20 | `CostingCode` | Edm.String | Yes | Costing Code | Norma de reparto (dimensión 1) |
| 21 | `ProjectCode` | Edm.String | Yes | Project Code | Código de proyecto |
| 22 | `BarCode` | Edm.String | Yes | Bar Code | Código de barras |
| 23 | `VatGroup` | Edm.String | Yes | Vat Group | Grupo de IVA (indicador de impuesto) |
| 24 | `Height1` | Edm.Double | Yes | Height 1 | Altura 1 |
| 25 | `Hight1Unit` | Edm.Int32 | Yes | Hight 1 Unit | Unidad de altura 1 |
| 26 | `Height2` | Edm.Double | Yes | Height 2 | Altura 2 |
| 27 | `Height2Unit` | Edm.Int32 | Yes | Height 2 Unit | Unidad de altura 2 |
| 28 | `Lengh1` | Edm.Double | Yes | Lengh 1 | Longitud 1 |
| 29 | `Lengh1Unit` | Edm.Int32 | Yes | Lengh 1 Unit | Unidad de longitud 1 |
| 30 | `Lengh2` | Edm.Double | Yes | Lengh 2 | Longitud 2 |
| 31 | `Lengh2Unit` | Edm.Int32 | Yes | Lengh 2 Unit | Unidad de longitud 2 |
| 32 | `Weight1` | Edm.Double | Yes | Weight 1 | Peso 1 |
| 33 | `Weight1Unit` | Edm.Int32 | Yes | Weight 1 Unit | Unidad de peso 1 |
| 34 | `Weight2` | Edm.Double | Yes | Weight 2 | Peso 2 |
| 35 | `Weight2Unit` | Edm.Int32 | Yes | Weight 2 Unit | Unidad de peso 2 |
| 36 | `Factor1` | Edm.Double | Yes | Factor 1 | Factor 1 |
| 37 | `Factor2` | Edm.Double | Yes | Factor 2 | Factor 2 |
| 38 | `Factor3` | Edm.Double | Yes | Factor 3 | Factor 3 |
| 39 | `Factor4` | Edm.Double | Yes | Factor 4 | Factor 4 |
| 40 | `BaseType` | Edm.Int32 | Yes | Base Type | Tipo base (tipo de objeto del documento base) |
| 41 | `BaseEntry` | Edm.Int32 | Yes | Base Entry | Entrada base (DocEntry del documento base) |
| 42 | `BaseLine` | Edm.Int32 | Yes | Base Line | Línea base (LineNum del documento base) |
| 43 | `Volume` | Edm.Double | Yes | Volume | Volumen |
| 44 | `VolumeUnit` | Edm.Int32 | Yes | Volume Unit | Unidad de volumen |
| 45 | `Width1` | Edm.Double | Yes | Width 1 | Ancho 1 |
| 46 | `Width1Unit` | Edm.Int32 | Yes | Width 1 Unit | Unidad de ancho 1 |
| 47 | `Width2` | Edm.Double | Yes | Width 2 | Ancho 2 |
| 48 | `Width2Unit` | Edm.Int32 | Yes | Width 2 Unit | Unidad de ancho 2 |
| 49 | `Address` | Edm.String | Yes | Address | Dirección |
| 50 | `TaxCode` | Edm.String | Yes | Tax Code | Indicador de impuesto |
| 51 | `TaxType` | [BoTaxTypes](../Enums/BoTaxTypes.md) | Yes | Tax Type | Tipo de impuesto |
| 52 | `TaxLiable` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Tax Liable | Sujeto a impuestos |
| 53 | `PickStatus` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Pick Status | Estado de picking |
| 54 | `PickQuantity` | Edm.Double | Yes | Pick Quantity | Cantidad de picking |
| 55 | `PickListIdNumber` | Edm.Int32 | Yes | Pick List ID Number | ID de la lista de picking |
| 56 | `OriginalItem` | Edm.String | Yes | Original Item | Artículo original |
| 57 | `BackOrder` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Back Order | Pedido pendiente (backorder) |
| 58 | `FreeText` | Edm.String | Yes | Free Text | Texto libre |
| 59 | `ShippingMethod` | Edm.Int32 | Yes | Shipping Method | Método de envío |
| 60 | `POTargetNum` | Edm.Int32 | Yes | PO Target Number | Número del pedido de compra destino |
| 61 | `POTargetEntry` | Edm.String | Yes | PO Target Entry | Entrada del pedido de compra destino |
| 62 | `POTargetRowNum` | Edm.Int32 | Yes | PO Target Row Number | Línea del pedido de compra destino |
| 63 | `CorrectionInvoiceItem` | [BoCorInvItemStatus](../Enums/BoCorInvItemStatus.md) | Yes | Correction Invoice Item | Artículo de factura de corrección |
| 64 | `CorrInvAmountToStock` | Edm.Double | Yes | Corr Inv Amount To Stock | Importe de factura de corrección a stock |
| 65 | `CorrInvAmountToDiffAcct` | Edm.Double | Yes | Corr Inv Amount To Diff Account | Importe de factura de corrección a cuenta de diferencias |
| 66 | `AppliedTax` | Edm.Double | Yes | Applied Tax | Impuesto aplicado |
| 67 | `AppliedTaxFC` | Edm.Double | Yes | Applied Tax FC (foreign currency) | Impuesto aplicado (ME) |
| 68 | `AppliedTaxSC` | Edm.Double | Yes | Applied Tax SC (system currency) | Impuesto aplicado (moneda del sistema) |
| 69 | `WTLiable` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Withholding Tax Liable | Sujeto a retención |
| 70 | `DeferredTax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Deferred Tax | Impuesto diferido |
| 71 | `EqualizationTaxPercent` | Edm.Double | Yes | Equalization Tax Percent | Porcentaje de recargo de equivalencia |
| 72 | `TotalEqualizationTax` | Edm.Double | Yes | Total Equalization Tax | Recargo de equivalencia total |
| 73 | `TotalEqualizationTaxFC` | Edm.Double | Yes | Total Equalization Tax FC (foreign currency) | Recargo de equivalencia total (ME) |
| 74 | `TotalEqualizationTaxSC` | Edm.Double | Yes | Total Equalization Tax SC (system currency) | Recargo de equivalencia total (moneda del sistema) |
| 75 | `NetTaxAmount` | Edm.Double | Yes | Net Tax Amount | Importe neto de impuestos |
| 76 | `NetTaxAmountFC` | Edm.Double | Yes | Net Tax Amount FC (foreign currency) | Importe neto de impuestos (ME) |
| 77 | `NetTaxAmountSC` | Edm.Double | Yes | Net Tax Amount SC (system currency) | Importe neto de impuestos (moneda del sistema) |
| 78 | `MeasureUnit` | Edm.String | Yes | Measure Unit | Unidad de medida |
| 79 | `UnitsOfMeasurment` | Edm.Double | Yes | Units Of Measurment | Unidades de medida |
| 80 | `LineTotal` | Edm.Double | Yes | Line Total | Total de línea |
| 81 | `TaxPercentagePerRow` | Edm.Double | Yes | Tax Percentage Per Row | Porcentaje de impuesto por línea |
| 82 | `TaxTotal` | Edm.Double | Yes | Tax Total | Total de impuestos |
| 83 | `ConsumerSalesForecast` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Consumer Sales Forecast | Previsión de ventas consumida |
| 84 | `ExciseAmount` | Edm.Double | Yes | Excise Amount | Importe de impuestos especiales |
| 85 | `TaxPerUnit` | Edm.Double | Yes | Tax Per Unit | Impuesto por unidad |
| 86 | `TotalInclTax` | Edm.Double | Yes | Total Incl Tax | Total con impuestos |
| 87 | `CountryOrg` | Edm.String | Yes | Country Org | País de origen |
| 88 | `SWW` | Edm.String | Yes | SWW | SWW (código de servicio) |
| 89 | `TransactionType` | [BoTransactionTypeEnum](../Enums/BoTransactionTypeEnum.md) | Yes | Transaction Type | Tipo de transacción |
| 90 | `DistributeExpense` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Distribute Expense | Distribuir gasto |
| 91 | `RowTotalFC` | Edm.Double | Yes | Row Total FC (foreign currency) | Total de línea (ME) |
| 92 | `RowTotalSC` | Edm.Double | Yes | Row Total SC (system currency) | Total de línea (moneda del sistema) |
| 93 | `LastBuyInmPrice` | Edm.Double | Yes | Last Buy Inm Price | Precio de la última compra |
| 94 | `LastBuyDistributeSumFc` | Edm.Double | Yes | Last Buy Distribute Sum Fc | Importe distribuido de la última compra (ME) |
| 95 | `LastBuyDistributeSumSc` | Edm.Double | Yes | Last Buy Distribute Sum Sc | Importe distribuido de la última compra (moneda del sistema) |
| 96 | `LastBuyDistributeSum` | Edm.Double | Yes | Last Buy Distribute Sum | Importe distribuido de la última compra |
| 97 | `StockDistributesumForeign` | Edm.Double | Yes | Stock Distributesum Foreign | Importe distribuido al stock (ME) |
| 98 | `StockDistributesumSystem` | Edm.Double | Yes | Stock Distributesum System | Importe distribuido al stock (moneda del sistema) |
| 99 | `StockDistributesum` | Edm.Double | Yes | Stock Distributesum | Importe distribuido al stock |
| 100 | `StockInmPrice` | Edm.Double | Yes | Stock Inm Price | Precio de stock |
| 101 | `PickStatusEx` | [BoDocumentLinePickStatus](../Enums/BoDocumentLinePickStatus.md) | Yes | Pick Status Ex | Estado de picking (ampliado) |
| 102 | `TaxBeforeDPM` | Edm.Double | Yes | Tax Before Down Payment | Impuesto antes de anticipos |
| 103 | `TaxBeforeDPMFC` | Edm.Double | Yes | Tax Before DPMFC | Impuesto antes de anticipos (ME) |
| 104 | `TaxBeforeDPMSC` | Edm.Double | Yes | Tax Before DPMSC | Impuesto antes de anticipos (moneda del sistema) |
| 105 | `CFOPCode` | Edm.String | Yes | CFOP Code | Código CFOP |
| 106 | `CSTCode` | Edm.String | Yes | CST Code | Código CST |
| 107 | `Usage` | Edm.Int32 | Yes | Usage | Uso |
| 108 | `TaxOnly` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Tax Only | Solo impuesto |
| 109 | `VisualOrder` | Edm.Int32 | Yes | Visual Order | Orden visual |
| 110 | `BaseOpenQuantity` | Edm.Double | Yes | Base Open Quantity | Cantidad abierta base |
| 111 | `UnitPrice` | Edm.Double | Yes | Unit Price | Precio unitario |
| 112 | `LineStatus` | [BoStatus](../Enums/BoStatus.md) | Yes | Line Status | Estado de línea |
| 113 | `PackageQuantity` | Edm.Double | Yes | Package Quantity | Cantidad de paquetes |
| 114 | `Text` | Edm.String | Yes | Text | Texto |
| 115 | `LineType` | [BoDocLineType](../Enums/BoDocLineType.md) | Yes | Line Type | Tipo de línea |
| 116 | `COGSCostingCode` | Edm.String | Yes | COGS Costing Code | Norma de reparto de costo de ventas |
| 117 | `COGSAccountCode` | Edm.String | Yes | COGS Account Code | Cuenta de costo de ventas |
| 118 | `ChangeAssemlyBoMWarehouse` | Edm.String | Yes | Change Assemly Bo M Warehouse | Cambiar almacén de la lista de materiales de ensamblaje |
| 119 | `GrossBuyPrice` | Edm.Double | Yes | Gross Buy Price | Precio de compra bruto |
| 120 | `GrossBase` | Edm.Int32 | Yes | Gross Base | Base bruta |
| 121 | `GrossProfitTotalBasePrice` | Edm.Double | Yes | Gross Profit Total Base Price | Precio base total del margen bruto |
| 122 | `CostingCode2` | Edm.String | Yes | Costing Code 2 | Norma de reparto (dimensión 2) |
| 123 | `CostingCode3` | Edm.String | Yes | Costing Code 3 | Norma de reparto (dimensión 3) |
| 124 | `CostingCode4` | Edm.String | Yes | Costing Code 4 | Norma de reparto (dimensión 4) |
| 125 | `CostingCode5` | Edm.String | Yes | Costing Code 5 | Norma de reparto (dimensión 5) |
| 126 | `ItemDetails` | Edm.String | Yes | Item Details | Detalles del artículo |
| 127 | `LocationCode` | Edm.Int32 | Yes | Location Code | Código de ubicación |
| 128 | `ActualDeliveryDate` | Edm.DateTimeOffset | Yes | Actual Delivery Date | Fecha real de entrega |
| 129 | `RemainingOpenQuantity` | Edm.Double | Yes | Remaining Open Quantity | Cantidad abierta restante |
| 130 | `OpenAmount` | Edm.Double | Yes | Open Amount | Importe abierto |
| 131 | `OpenAmountFC` | Edm.Double | Yes | Open Amount FC (foreign currency) | Importe abierto (ME) |
| 132 | `OpenAmountSC` | Edm.Double | Yes | Open Amount SC (system currency) | Importe abierto (moneda del sistema) |
| 133 | `ExLineNo` | Edm.String | Yes | Ex Line Number | Número de línea externo |
| 134 | `RequiredDate` | Edm.DateTimeOffset | Yes | Required Date | Fecha requerida |
| 135 | `RequiredQuantity` | Edm.Double | Yes | Required Quantity | Cantidad requerida |
| 136 | `COGSCostingCode2` | Edm.String | Yes | COGS Costing Code 2 | Norma de reparto de costo de ventas 2 |
| 137 | `COGSCostingCode3` | Edm.String | Yes | COGS Costing Code 3 | Norma de reparto de costo de ventas 3 |
| 138 | `COGSCostingCode4` | Edm.String | Yes | COGS Costing Code 4 | Norma de reparto de costo de ventas 4 |
| 139 | `COGSCostingCode5` | Edm.String | Yes | COGS Costing Code 5 | Norma de reparto de costo de ventas 5 |
| 140 | `CSTforIPI` | Edm.String | Yes | CS Tfor IPI | CST para IPI |
| 141 | `CSTforPIS` | Edm.String | Yes | CS Tfor PIS | CST para PIS |
| 142 | `CSTforCOFINS` | Edm.String | Yes | CS Tfor COFINS | CST para COFINS |
| 143 | `CreditOriginCode` | Edm.String | Yes | Credit Origin Code | Código de origen del crédito |
| 144 | `WithoutInventoryMovement` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Without Inventory Movement | Sin movimiento de inventario |
| 145 | `AgreementNo` | Edm.Int32 | Yes | Agreement Number | Número de acuerdo |
| 146 | `AgreementRowNumber` | Edm.Int32 | Yes | Agreement Row Number | Número de línea del acuerdo |
| 147 | `ActualBaseEntry` | Edm.Int32 | Yes | Actual Base Entry | Entrada base real |
| 148 | `ActualBaseLine` | Edm.Int32 | Yes | Actual Base Line | Línea base real |
| 149 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 150 | `Surpluses` | Edm.Double | Yes | Surpluses | Excedentes |
| 151 | `DefectAndBreakup` | Edm.Double | Yes | Defect And Breakup | Defectos y roturas |
| 152 | `Shortages` | Edm.Double | Yes | Shortages | Faltantes |
| 153 | `ConsiderQuantity` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Consider Quantity | Considerar cantidad |
| 154 | `PartialRetirement` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Partial Retirement | Baja parcial |
| 155 | `RetirementQuantity` | Edm.Double | Yes | Retirement Quantity | Cantidad dada de baja |
| 156 | `RetirementAPC` | Edm.Double | Yes | Retirement APC | Costo de adquisición de la baja |
| 157 | `ThirdParty` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Third Party | Tercero |
| 158 | `PoNum` | Edm.String | Yes | Po Number | Número de pedido de compra |
| 159 | `PoItmNum` | Edm.Int32 | Yes | Po Itm Number | Número de artículo del pedido de compra |
| 160 | `ExpenseType` | Edm.String | Yes | Expense Type | Tipo de gasto |
| 161 | `ReceiptNumber` | Edm.String | Yes | Receipt Number | Número de recibo |
| 162 | `ExpenseOperationType` | [BoExpenseOperationTypeEnum](../Enums/BoExpenseOperationTypeEnum.md) | Yes | Expense Operation Type | Tipo de operación de gasto |
| 163 | `FederalTaxID` | Edm.String | Yes | Federal Tax ID | CUIT / ID fiscal federal |
| 164 | `GrossProfit` | Edm.Double | Yes | Gross Profit | Margen bruto |
| 165 | `GrossProfitFC` | Edm.Double | Yes | Gross Profit FC (foreign currency) | Margen bruto (ME) |
| 166 | `GrossProfitSC` | Edm.Double | Yes | Gross Profit SC (system currency) | Margen bruto (moneda del sistema) |
| 167 | `PriceSource` | [DocumentPriceSourceEnum](../Enums/DocumentPriceSourceEnum.md) | Yes | Price Source | Origen del precio |
| 168 | `EnableReturnCost` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Return Cost | Habilitar costo de devolución |
| 169 | `ReturnCost` | Edm.Double | Yes | Return Cost | Costo de devolución |
| 170 | `LineVendor` | Edm.String | Yes | Line Vendor | Proveedor de la línea |
| 171 | `ReturnAction` | Edm.Int32 | Yes | Return Action | Acción de devolución |
| 172 | `ReturnReason` | Edm.Int32 | Yes | Return Reason | Motivo de devolución |
| 173 | `StgSeqNum` | Edm.Int32 | Yes | Stg Seq Number | Número de secuencia de etapa |
| 174 | `StgEntry` | Edm.Int32 | Yes | Stg Entry | Entrada de etapa |
| 175 | `StgDesc` | Edm.String | Yes | Stg Description | Descripción de etapa |
| 176 | `UoMEntry` | Edm.Int32 | Yes | Uo M Entry | Entrada de unidad de medida (UomEntry) |
| 177 | `UoMCode` | Edm.String | Yes | Uo M Code | Código de unidad de medida |
| 178 | `InventoryQuantity` | Edm.Double | Yes | Inventory Quantity | Cantidad de inventario |
| 179 | `RemainingOpenInventoryQuantity` | Edm.Double | Yes | Remaining Open Inventory Quantity | Cantidad de inventario abierta restante |
| 180 | `ParentLineNum` | Edm.Int32 | Yes | Parent Line Number | Número de línea padre |
| 181 | `Incoterms` | Edm.Int32 | Yes | Incoterms | Incoterms |
| 182 | `TransportMode` | Edm.Int32 | Yes | Transport Mode | Modo de transporte |
| 183 | `NatureOfTransaction` | Edm.Int32 | Yes | Nature Of Transaction | Naturaleza de la transacción |
| 184 | `DestinationCountryForImport` | Edm.String | Yes | Destination Country For Import | País de destino de la importación |
| 185 | `DestinationRegionForImport` | Edm.Int32 | Yes | Destination Region For Import | Región de destino de la importación |
| 186 | `OriginCountryForExport` | Edm.String | Yes | Origin Country For Export | País de origen de la exportación |
| 187 | `OriginRegionForExport` | Edm.Int32 | Yes | Origin Region For Export | Región de origen de la exportación |
| 188 | `ItemType` | [BoDocItemType](../Enums/BoDocItemType.md) | Yes | Item Type | Tipo de artículo |
| 189 | `ChangeInventoryQuantityIndependently` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Change Inventory Quantity Independently | Modificar cantidad de inventario de forma independiente |
| 190 | `FreeOfChargeBP` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Free Of Charge Business Partner | Socio de negocios sin cargo |
| 191 | `SACEntry` | Edm.Int32 | Yes | SAC Entry | Entrada SAC |
| 192 | `HSNEntry` | Edm.Int32 | Yes | HSN Entry | Entrada HSN |
| 193 | `GrossPrice` | Edm.Double | Yes | Gross Price | Precio bruto |
| 194 | `GrossTotal` | Edm.Double | Yes | Gross Total | Total bruto |
| 195 | `GrossTotalFC` | Edm.Double | Yes | Gross Total FC (foreign currency) | Total bruto (ME) |
| 196 | `GrossTotalSC` | Edm.Double | Yes | Gross Total SC (system currency) | Total bruto (moneda del sistema) |
| 197 | `NCMCode` | Edm.Int32 | Yes | NCM Code | Código NCM |
| 198 | `NVECode` | Edm.String | Yes | NVE Code | Código NVE |
| 199 | `IndEscala` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Ind Escala | Indicador de escala relevante (Brasil) |
| 200 | `CtrSealQty` | Edm.Double | Yes | Ctr Seal Quantity | Cantidad de precintos del contenedor |
| 201 | `CNJPMan` | Edm.String | Yes | CNJP Man | CNPJ del fabricante |
| 202 | `CESTCode` | Edm.Int32 | Yes | CEST Code | Código CEST |
| 203 | `UFFiscalBenefitCode` | Edm.String | Yes | UF Fiscal Benefit Code | Código de beneficio fiscal UF (Brasil) |
| 204 | `ReverseCharge` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Reverse Charge | Inversión del sujeto pasivo |
| 205 | `ShipToCode` | Edm.String | Yes | Ship To Code | Código de dirección de envío |
| 206 | `ShipToDescription` | Edm.String | Yes | Ship To Description | Descripción de la dirección de envío |
| 207 | `ShipFromCode` | Edm.String | Yes | Ship From Code | Código de dirección de origen |
| 208 | `ShipFromDescription` | Edm.String | Yes | Ship From Description | Descripción del origen del envío |
| 209 | `OwnerCode` | Edm.Int32 | Yes | Owner Code | Código del titular |
| 210 | `ExternalCalcTaxRate` | Edm.Double | Yes | External Calc Tax Rate | Tasa de impuesto calculada externamente |
| 211 | `ExternalCalcTaxAmount` | Edm.Double | Yes | External Calc Tax Amount | Importe de impuesto calculado externamente |
| 212 | `ExternalCalcTaxAmountFC` | Edm.Double | Yes | External Calc Tax Amount FC (foreign currency) | Importe de impuesto calculado externamente (ME) |
| 213 | `ExternalCalcTaxAmountSC` | Edm.Double | Yes | External Calc Tax Amount SC (system currency) | Importe de impuesto calculado externamente (moneda del sistema) |
| 214 | `StandardItemIdentification` | Edm.Int32 | Yes | Standard Item Identification | Identificación estándar del artículo |
| 215 | `CommodityClassification` | Edm.Int32 | Yes | Commodity Classification | Clasificación de mercancía |
| 216 | `WeightOfRecycledPlastic` | Edm.Double | Yes | Weight Of Recycled Plastic | Peso de plástico reciclado |
| 217 | `PlasticPackageExemptionReason` | Edm.String | Yes | Plastic Package Exemption Reason | Motivo de exención de envases plásticos |
| 218 | `LegalText` | Edm.String | Yes | Legal Text | Texto legal |
| 219 | `Cig` | Edm.Int32 | Yes | Cig | Código CIG |
| 220 | `Cup` | Edm.Int32 | Yes | Cup | Código CUP |
| 221 | `OperatingProfit` | Edm.Double | Yes | Operating Profit | Beneficio operativo |
| 222 | `OperatingProfitFC` | Edm.Double | Yes | Operating Profit FC (foreign currency) | Beneficio operativo (ME) |
| 223 | `OperatingProfitSC` | Edm.Double | Yes | Operating Profit SC (system currency) | Beneficio operativo (moneda del sistema) |
| 224 | `NetIncome` | Edm.Double | Yes | Net Income | Ingreso neto |
| 225 | `NetIncomeFC` | Edm.Double | Yes | Net Income FC (foreign currency) | Ingreso neto (ME) |
| 226 | `NetIncomeSC` | Edm.Double | Yes | Net Income SC (system currency) | Ingreso neto (moneda del sistema) |
| 227 | `CSTforIBS` | Edm.String | Yes | CS Tfor IBS | CST para IBS |
| 228 | `CSTforCBS` | Edm.String | Yes | CS Tfor CBS | CST para CBS |
| 229 | `CSTforIS` | Edm.String | Yes | CS Tfor IS | CST para IS |
| 230 | `UnencumberedReason` | Edm.Int32 | Yes | Unencumbered Reason | Motivo de no gravado |
| 231 | `CUSplit` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | CU Split | División CU |
| 232 | `ListNum` | Edm.Int32 | Yes | List Number | Número de lista de precios |
| 233 | `RecognizedTaxCode` | Edm.String | Yes | Recognized Tax Code | Indicador de impuesto reconocido |
| 234 | `LineTaxJurisdictions` | Collection([LineTaxJurisdiction](../Tipos-Complejos/LineTaxJurisdiction.md)) | Yes | Line Tax Jurisdictions | Jurisdicciones fiscales de línea |
| 235 | `GeneratedAssets` | Collection([GeneratedAsset](../Tipos-Complejos/GeneratedAsset.md)) | Yes | Generated Assets | Activos generados |
| 236 | `EBooksDetails` | Collection([EBooksDetail](../Tipos-Complejos/EBooksDetail.md)) | Yes | E Books Details | Detalles de libros electrónicos |
| 237 | `DocLinePickLists` | Collection([DocLinePickList](../Tipos-Complejos/DocLinePickList.md)) | Yes | Document Line Pick Lists | Listas de picking de la línea del documento |
| 238 | `DocumentLineAdditionalExpenses` | Collection([DocumentLineAdditionalExpense](../Tipos-Complejos/DocumentLineAdditionalExpense.md)) | Yes | Document Line Additional Expenses | Gastos adicionales de la línea del documento |
| 239 | `WithholdingTaxLines` | Collection([WithholdingTaxLine](../Tipos-Complejos/WithholdingTaxLine.md)) | Yes | Withholding Tax Lines | Líneas de retenciones |
| 240 | `SerialNumbers` | Collection([SerialNumber](../Tipos-Complejos/SerialNumber.md)) | Yes | Serial Numbers | Números de serie |
| 241 | `BatchNumbers` | Collection([BatchNumber](../Tipos-Complejos/BatchNumber.md)) | Yes | Batch Numbers | Números de lote |
| 242 | `DocumentLinesBinAllocations` | Collection([DocumentLinesBinAllocation](../Tipos-Complejos/DocumentLinesBinAllocation.md)) | Yes | Document Lines Bin Allocations | Asignaciones de ubicaciones de las líneas |
| 243 | `ExportProcesses` | Collection([ExportProcess](../Tipos-Complejos/ExportProcess.md)) | Yes | Export Processes | Procesos de exportación |
| 244 | `CCDNumbers` | Collection([CCDNumber](../Tipos-Complejos/CCDNumber.md)) | Yes | CCD Numbers | Números de declaración aduanera de carga |
| 245 | `ImportProcesses` | Collection([ImportProcess](../Tipos-Complejos/ImportProcess.md)) | Yes | Import Processes | Procesos de importación |

## Used by (properties)

- [Document](../Entidades/PurchaseQuotations.md).`DocumentLines`
