# AdminInfo — Datos de administración (configuración general)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `AdminInfo`
- **Descripción (ES):** Datos de administración (configuración general)
- **Description (EN):** Admin Information

- **Properties:** 277

## Properties (277)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` | Edm.Int32 | Yes | Code | Código |
| 2 | `CompanyName` | Edm.String | Yes | Company Name | Nombre de la sociedad |
| 3 | `Address` | Edm.String | Yes | Address | Dirección |
| 4 | `Country` | Edm.String | Yes | Country | País |
| 5 | `PrintingHeader` | Edm.String | Yes | Printing Header | Encabezado de impresión |
| 6 | `PhoneNumber1` | Edm.String | Yes | Phone Number 1 | Número de teléfono 1 |
| 7 | `PhoneNumber2` | Edm.String | Yes | Phone Number 2 | Número de teléfono 2 |
| 8 | `FaxNumber` | Edm.String | Yes | Fax Number | Número de fax |
| 9 | `eMail` | Edm.String | Yes | E Mail | Correo electrónico |
| 10 | `ManagingDirector` | Edm.String | Yes | Managing Director | Director general |
| 11 | `ChartofAccountsTemplate` | Edm.String | Yes | Chartof Accounts Template | Plantilla del plan de cuentas |
| 12 | `LocalCurrency` | Edm.String | Yes | Local Currency | Moneda local |
| 13 | `SystemCurrency` | Edm.String | Yes | System Currency | Moneda del sistema |
| 14 | `CreditBalancewithMinusSign` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Credit Balancewith Minus Sign | Saldo acreedor con signo negativo |
| 15 | `StandardUnitofLength` | Edm.Int32 | Yes | Standard Unitof Length | Unidad de longitud estándar |
| 16 | `WeightUnitDefault` | Edm.Int32 | Yes | Weight Unit Default | Unidad de peso predeterminada |
| 17 | `DirectIndirectRate` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Direct Indirect Rate | Tasa directa/indirecta |
| 18 | `MinimumAmountfor347Report` | Edm.Double | Yes | Minimum Amountfor 347 Report | Importe mínimo para modelo 347 |
| 19 | `SetItemsWarehouses` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Set Items Warehouses | Asignar almacenes a artículos |
| 20 | `BankCountry` | Edm.String | Yes | Bank Country | País del banco |
| 21 | `FederalTaxID` | Edm.String | Yes | Federal Tax ID | CUIT / ID fiscal federal |
| 22 | `TaxOffice` | Edm.String | Yes | Tax Office | Oficina tributaria |
| 23 | `DeductionFileNo` | Edm.String | Yes | Deduction File Number | Número de expediente de deducción |
| 24 | `TaxCollection` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Tax Collection | Colección de impuestos |
| 25 | `TaxDefinition` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Tax Definition | Definición de impuestos |
| 26 | `TaxPercentage` | Edm.Double | Yes | Tax Percentage | Porcentaje de impuesto |
| 27 | `AdvancesonCorpIncomeTax` | Edm.Double | Yes | Advanceson Corp Income Tax | Anticipos de impuesto a las ganancias de sociedades |
| 28 | `WithTax` | Edm.Double | Yes | With Tax | Con impuestos |
| 29 | `WithholdingTaxVendorDdct` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Withholding Tax Vendor Ddct | Deducción de retención del proveedor |
| 30 | `CustomersDeductionatSource` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Customers Deductionat Source | Retención en la fuente de clientes |
| 31 | `WithholdingTaxTdctPercnt` | Edm.Double | Yes | Withholding Tax Tdct Percnt | Porcentaje de deducción de retención |
| 32 | `WithholdingTaxDdctExpired` | Edm.DateTimeOffset | Yes | Withholding Tax Ddct Expired | Deducción de retención vencida |
| 33 | `WithholdingTaxDdctOffice` | Edm.String | Yes | Withholding Tax Ddct Office | Oficina de deducción de retención |
| 34 | `CommitmentRestriction` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Commitment Restriction | Restricción de compromiso |
| 35 | `CreditRestriction` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Credit Restriction | Restricción de crédito |
| 36 | `RestrictSales` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Restrict Sales | Restringir ventas |
| 37 | `RestrictDelNotesPO` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Restrict Del Notes PO | Restringir entregas de pedidos de compra |
| 38 | `RestrictOrders` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Restrict Orders | Restringir pedidos |
| 39 | `ConsiderDelNotesinSalesR` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Consider Del Notesin Sales R | Considerar entregas en informes de ventas |
| 40 | `CreditDepositType` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Credit Deposit Type | Tipo de depósito de tarjetas de crédito |
| 41 | `UseTax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Use Tax | Impuesto de uso |
| 42 | `SplitPO` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Split PO | Dividir pedido de compra |
| 43 | `AltNameForApInvoice` | Edm.String | Yes | Alt Name For Ap Invoice | Nombre alternativo para factura de proveedores |
| 44 | `AltNameforCreditMemo` | Edm.String | Yes | Alt Namefor Credit Memo | Nombre alternativo para nota de crédito |
| 45 | `AltNameForGoodsReceipt` | Edm.String | Yes | Alt Name For Goods Receipt | Nombre alternativo para entrada de mercancías |
| 46 | `AltNameForGoodsReturn` | Edm.String | Yes | Alt Name For Goods Return | Nombre alternativo para devolución de mercancías |
| 47 | `AltNameForPurchase` | Edm.String | Yes | Alt Name For Purchase | Nombre alternativo para compras |
| 48 | `AlertTypeforWHStock` | [BoAlertTypeforWHStockEnum](../Enums/BoAlertTypeforWHStockEnum.md) | Yes | Alert Typefor Warehouse Stock | Tipo de alerta para stock de almacén |
| 49 | `SetCommissionbyCustomer` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Set Commissionby Customer | Fijar comisión por cliente |
| 50 | `SetCommissionbyItem` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Set Commissionby Item | Fijar comisión por artículo |
| 51 | `SetCommissionbySE` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Set Commissionby SE | Fijar comisión por empleado de ventas |
| 52 | `DefaultCustomerPaymentTerms` | Edm.Int32 | Yes | Default Customer Payment Terms | Condiciones de pago predeterminadas de clientes |
| 53 | `DefaultVendorPaymentTerms` | Edm.Int32 | Yes | Default Vendor Payment Terms | Condiciones de pago predeterminadas de proveedores |
| 54 | `CalculateGrossProfitperTra` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Calculate Gross Profitper Tra | Calcular margen bruto por transacción |
| 55 | `PriceListforCostPrice` | Edm.Int32 | Yes | Price Listfor Cost Price | Lista de precios para precio de costo |
| 56 | `GrossProfitAfterSale` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Gross Profit After Sale | Margen bruto después de la venta |
| 57 | `DisplayPriceforPriceOnly` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Display Pricefor Price Only | Mostrar precio solo para precio |
| 58 | `CalculateTaxinSalesQuotati` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Calculate Taxin Sales Quotati | Calcular impuestos en ofertas de ventas |
| 59 | `BaseField` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Base Field | Campo base |
| 60 | `AllowClosedSalesQuotations` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Allow Closed Sales Quotations | Permitir ofertas de ventas cerradas |
| 61 | `UserConversionCode` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | User Conversion Code | Código de conversión del usuario |
| 62 | `CompanyColor` | Edm.Int32 | Yes | Company Color | Color de la sociedad |
| 63 | `TotalsAccuracy` | Edm.Int32 | Yes | Totals Accuracy | Precisión de totales |
| 64 | `AccuracyofQuantities` | Edm.Int32 | Yes | Accuracyof Quantities | Precisión de cantidades (decimales) |
| 65 | `PriceAccuracy` | Edm.Int32 | Yes | Price Accuracy | Precisión de precios |
| 66 | `RateAccuracy` | Edm.Int32 | Yes | Rate Accuracy | Precisión de tipos de cambio |
| 67 | `PercentageAccuracy` | Edm.Int32 | Yes | Percentage Accuracy | Precisión de porcentajes |
| 68 | `MeasuringAccuracy` | Edm.Int32 | Yes | Measuring Accuracy | Precisión de medición |
| 69 | `QueryAccuracy` | Edm.Int32 | Yes | Query Accuracy | Precisión de consultas |
| 70 | `AddressinForeignLanguage` | Edm.String | Yes | Addressin Foreign Language | Dirección en idioma extranjero |
| 71 | `DefaultTaxCode` | Edm.String | Yes | Default Tax Code | Indicador de impuesto predeterminado |
| 72 | `LetterHeaderinForeignLangu` | Edm.String | Yes | Letter Headerin Foreign Langu | Encabezado de carta en idioma extranjero |
| 73 | `PhoneNumber1ForeignLang` | Edm.String | Yes | Phone Number 1 Foreign Lang | Número de teléfono 1 (idioma extranjero) |
| 74 | `PhoneNumber2ForeignLang` | Edm.String | Yes | Phone Number 2 Foreign Lang | Número de teléfono 2 (idioma extranjero) |
| 75 | `FaxNumberForeignLang` | Edm.String | Yes | Fax Number Foreign Lang | Número de fax (idioma extranjero) |
| 76 | `ManagingDirectorForeignLan` | Edm.String | Yes | Managing Director Foreign Lan | Director general (idioma extranjero) |
| 77 | `TimeTemplate` | [BoTimeTemplate](../Enums/BoTimeTemplate.md) | Yes | Time Template | Plantilla de hora |
| 78 | `DateTemplate` | [BoDateTemplate](../Enums/BoDateTemplate.md) | Yes | Date Template | Plantilla de fecha |
| 79 | `DateSeparator` | Edm.String | Yes | Date Separator | Separador de fecha |
| 80 | `FCCheckAccount` | [BoCurrencyCheck](../Enums/BoCurrencyCheck.md) | Yes | FC (foreign currency) Check Account | Cuenta de cheques (ME) |
| 81 | `ChangedExistingOrders` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Changed Existing Orders | Pedidos existentes modificados |
| 82 | `MultiCurrencyCheck` | [BoCurrencyCheck](../Enums/BoCurrencyCheck.md) | Yes | Multi Currency Check | Verificación multimoneda |
| 83 | `ISRType` | Edm.Int32 | Yes | ISR Type | Tipo ISR |
| 84 | `DisplayRoundingRemark` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Display Rounding Remark | Mostrar comentario de redondeo |
| 85 | `ISRBillerID` | Edm.String | Yes | ISR Biller ID | ID de facturador ISR |
| 86 | `BlockSystemCurrencyEditing` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Block System Currency Editing | Bloquear edición de moneda del sistema |
| 87 | `BlockPostingDateEditing` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Block Posting Date Editing | Bloquear edición de fecha de contabilización |
| 88 | `DefaultWarehouse` | Edm.String | Yes | Default Warehouse | Almacén predeterminado |
| 89 | `BlockTaxDate` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Block Tax Date | Bloquear fecha de impuestos |
| 90 | `TaxDefinitionforVatitem` | Edm.String | Yes | Tax Definitionfor Vatitem | Definición de impuestos para artículos con IVA |
| 91 | `TaxDefinitionforVatservice` | Edm.String | Yes | Tax Definitionfor Vatservice | Definición de impuestos para servicios con IVA |
| 92 | `TaxGroupforPurchaseItem` | Edm.String | Yes | Tax Groupfor Purchase Item | Grupo de impuestos para artículos de compra |
| 93 | `TaxGroupforServicePurchase` | Edm.String | Yes | Tax Groupfor Service Purchase | Grupo de impuestos para compra de servicios |
| 94 | `CalculateBudget` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Calculate Budget | Calcular presupuesto |
| 95 | `CustomerIdNumber` | Edm.String | Yes | Customer ID Number | Número de identificación del cliente |
| 96 | `BlockBudget` | [BoBlockBudget](../Enums/BoBlockBudget.md) | Yes | Block Budget | Bloquear presupuesto |
| 97 | `BudgetAlert` | [BoBudgetAlert](../Enums/BoBudgetAlert.md) | Yes | Budget Alert | Alerta de presupuesto |
| 98 | `BlockPurchaseOrders` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Block Purchase Orders | Bloquear pedidos de compra |
| 99 | `BlockBookkeeping` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Block Bookkeeping | Bloquear contabilidad |
| 100 | `DefaultBudgetCostAssessMt` | Edm.Int32 | Yes | Default Budget Cost Assess Mt | Método de asignación de costos de presupuesto predeterminado |
| 101 | `ContinuousStockManagement` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Continuous Stock Management | Gestión de stock permanente |
| 102 | `ContinuousStockSystem` | [BoInventorySystem](../Enums/BoInventorySystem.md) | Yes | Continuous Stock System | Sistema de stock permanente |
| 103 | `RoundTaxAmounts` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Round Tax Amounts | Redondear importes de impuestos |
| 104 | `BlockDelNotesforPurchase` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Block Del Notesfor Purchase | Bloquear entregas para compras |
| 105 | `FileNumberinIncomeTax` | Edm.String | Yes | File Numberin Income Tax | Número de expediente en impuesto a las ganancias |
| 106 | `DeferredTax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Deferred Tax | Impuesto diferido |
| 107 | `DefaultBankNo` | Edm.String | Yes | Default Bank Number | Número de banco predeterminado |
| 108 | `DefaultBankAccount` | Edm.String | Yes | Default Bank Account | Cuenta bancaria predeterminada |
| 109 | `DefaultBranch` | Edm.String | Yes | Default Branch | Sucursal predeterminada |
| 110 | `UsePASystem` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Use PA System | Usar sistema PA |
| 111 | `ServiceCode` | Edm.String | Yes | Service Code | Código de servicio |
| 112 | `ServicePassword` | Edm.String | Yes | Service Password | Contraseña del servicio |
| 113 | `ParamFolderPath` | Edm.String | Yes | Parameter Folder Path | Ruta de carpeta de parámetros |
| 114 | `ExcelFolderPath` | Edm.String | Yes | Excel Folder Path | Ruta de carpeta de Excel |
| 115 | `FederalTaxID2` | Edm.String | Yes | Federal Tax ID 2 | ID fiscal federal 2 |
| 116 | `FederalTaxID3` | Edm.String | Yes | Federal Tax ID 3 | ID fiscal federal 3 |
| 117 | `DecimalSeparator` | Edm.String | Yes | Decimal Separator | Separador decimal |
| 118 | `ThousandsSeparator` | Edm.String | Yes | Thousands Separator | Separador de miles |
| 119 | `DisplayCurrencyontheRight` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Display Currencyonthe Right | Mostrar moneda a la derecha |
| 120 | `AlertbyWarehouse` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Alertby Warehouse | Alerta por almacén |
| 121 | `PriceSystem` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Price System | Sistema de precios |
| 122 | `WholdingTaxDedHierarchy` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Wholding Tax Ded Hierarchy | Jerarquía de deducción de retenciones |
| 123 | `DocConfirmation` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Document Confirmation | Confirmación del documento |
| 124 | `DefaultforBatchStatus` | [BoDefaultBatchStatus](../Enums/BoDefaultBatchStatus.md) | Yes | Defaultfor Batch Status | Estado de lote predeterminado |
| 125 | `GLMethod` | [BoGLMethods](../Enums/BoGLMethods.md) | Yes | G/L Method | Método de cuentas de mayor (por almacén/grupo/artículo) |
| 126 | `UniqueSerialNo` | [BoUniqueSerialNumber](../Enums/BoUniqueSerialNumber.md) | Yes | Unique Serial Number | Número de serie único |
| 127 | `MaxHistory` | Edm.Int32 | Yes | Max History | Historial máximo |
| 128 | `ChangeDefReconAPAccounts` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Change Default Recon AP Accounts | Cambiar cuentas de conciliación predeterminadas (compras) |
| 129 | `ChangeDefReconARAccounts` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Change Default Recon AR Accounts | Cambiar cuentas de conciliación predeterminadas (ventas) |
| 130 | `BPTypeCode` | Edm.String | Yes | Business Partner Type Code | Código de tipo de socio de negocios |
| 131 | `PBSNumber` | Edm.String | Yes | PBS Number | Número PBS |
| 132 | `PBSGroupNumber` | Edm.String | Yes | PBS Group Number | Número de grupo PBS |
| 133 | `OrganizationNumber` | Edm.String | Yes | Organization Number | Número de organización |
| 134 | `AccountSegmentsSeparator` | Edm.String | Yes | Account Segments Separator | Separador de segmentos de cuenta |
| 135 | `DisplayBookkeepingWindow` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Display Bookkeeping Window | Mostrar ventana de contabilización |
| 136 | `SHandleWT` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | S Handle Withholding Tax | Gestionar retención (ventas) |
| 137 | `SDefaultWTCode` | Edm.String | Yes | S Default Withholding Tax Code | Código de retención predeterminado (ventas) |
| 138 | `WithholdingTaxPHandle` | Edm.String | Yes | Withholding Tax P Handle | Gestionar retención (compras) |
| 139 | `PDefaultWTCode` | Edm.String | Yes | P Default Withholding Tax Code | Código de retención predeterminado (compras) |
| 140 | `WTLiableExpense` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Withholding Tax Liable Expense | Gasto sujeto a retención |
| 141 | `UseNegativeAmounts` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Use Negative Amounts | Usar importes negativos |
| 142 | `HolidaysName` | Edm.String | Yes | Holidays Name | Nombre de festivos |
| 143 | `OrderBlock` | Edm.String | Yes | Order Block | Bloqueo de pedidos |
| 144 | `RoundingMethod` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Rounding Method | Método de redondeo |
| 145 | `AdressFromWH` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Adress From Warehouse | Dirección desde el almacén |
| 146 | `OrderingParty` | Edm.String | Yes | Ordering Party | Ordenante |
| 147 | `CertificateNo` | Edm.String | Yes | Certificate Number | Número de certificado |
| 148 | `ExpirationDate` | Edm.DateTimeOffset | Yes | Expiration Date | Fecha de vencimiento |
| 149 | `NationalInsuranceNo` | Edm.String | Yes | National Insurance Number | Número de seguridad social |
| 150 | `SalesOrderConfirmed` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Sales Order Confirmed | Pedido de cliente confirmado |
| 151 | `PurchaseOrderConfirmed` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Purchase Order Confirmed | Pedido de compra confirmado |
| 152 | `SDfltITWT` | Edm.String | Yes | S Default ITWT | Retención predeterminada IT (ventas) |
| 153 | `PDfltITWT` | Edm.String | Yes | P Default ITWT | Retención predeterminada IT (compras) |
| 154 | `DefaultAccountCurrency` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Default Account Currency | Moneda predeterminada de la cuenta |
| 155 | `DeferredTaxforVendors` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Deferred Taxfor Vendors | Impuesto diferido para proveedores |
| 156 | `CreateAutoVATLineinJDT` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Create Auto VAT Linein JDT | Crear línea de IVA automática en el asiento |
| 157 | `ConsumeForecast` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Consume Forecast | Consumir previsión |
| 158 | `ConsumptionMethod` | [BoConsumptionMethod](../Enums/BoConsumptionMethod.md) | Yes | Consumption Method | Método de consumo |
| 159 | `DaysBackward` | Edm.Int32 | Yes | Days Backward | Días hacia atrás |
| 160 | `DaysForward` | Edm.Int32 | Yes | Days Forward | Días hacia adelante |
| 161 | `DefaultDunningTerm` | Edm.String | Yes | Default Dunning Term | Condición de reclamación predeterminada |
| 162 | `DefaultBankAccountKey` | Edm.Int32 | Yes | Default Bank Account Key | Clave de cuenta bancaria predeterminada |
| 163 | `MultiLanguageSupportEnable` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Multi Language Support Enable | Soporte multilingüe habilitado |
| 164 | `AllowFuturePostingDate` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Allow Future Posting Date | Permitir fecha de contabilización futura |
| 165 | `AdditionalIdNumber` | Edm.String | Yes | Additional ID Number | Número de identificación adicional |
| 166 | `State` | Edm.String | Yes | State | Estado/provincia |
| 167 | `CalculateRowDiscount` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Calculate Row Discount | Calcular descuento de línea |
| 168 | `BankStatementInstalled` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Bank Statement Installed | Extracto bancario instalado |
| 169 | `EnableDigitalPayments` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Digital Payments | Habilitar pagos digitales |
| 170 | `UniqueTaxPayerReference` | Edm.String | Yes | Unique Tax Payer Reference | Referencia única del contribuyente |
| 171 | `EmployerReference` | Edm.String | Yes | Employer Reference | Referencia del empleador |
| 172 | `PeriodStatusAutoChange` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Period Status Auto Change | Cambio automático del estado del período |
| 173 | `PeriodStatusChangeDelay` | Edm.Int32 | Yes | Period Status Change Delay | Retraso del cambio de estado del período |
| 174 | `GrossProfitPercentForServiceDocuments` | Edm.Double | Yes | Gross Profit Percent For Service Documents | Porcentaje de margen bruto para documentos de servicio |
| 175 | `XMLFileFolderPath` | Edm.String | Yes | XML File Folder Path | Ruta de carpeta de archivos XML |
| 176 | `PickList` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Pick List | Lista de picking |
| 177 | `GeneralManager` | Edm.String | Yes | General Manager | Gerente general |
| 178 | `GeneralManagerForeignLanguage` | Edm.String | Yes | General Manager Foreign Language | Gerente general (idioma extranjero) |
| 179 | `UseProductionProfitAndLossAccount` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Use Production Profit And Loss Account | Usar cuenta de pérdidas y ganancias de producción |
| 180 | `WTAccumAmountAP` | Edm.Double | Yes | Withholding Tax Accum Amount AP | Importe de retención acumulado (compras) |
| 181 | `WTAccumAmountAR` | Edm.Double | Yes | Withholding Tax Accum Amount AR | Importe de retención acumulado (ventas) |
| 182 | `CopyExchangeRateInCopyTo` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Copy Exchange Rate In Copy To | Copiar tipo de cambio al copiar a |
| 183 | `GTSOutboundFolder` | Edm.String | Yes | GTS Outbound Folder | Carpeta de salida GTS |
| 184 | `GTSInboundFolder` | Edm.String | Yes | GTS Inbound Folder | Carpeta de entrada GTS |
| 185 | `GTSSeparateCode` | Edm.String | Yes | GTS Separate Code | Código separado GTS |
| 186 | `GTSDefaultChecker` | Edm.Int32 | Yes | GTS Default Checker | Verificador GTS predeterminado |
| 187 | `GTSDefaultPayee` | Edm.Int32 | Yes | GTS Default Payee | Beneficiario GTS predeterminado |
| 188 | `GTSMaxAmount` | Edm.Double | Yes | GTS Max Amount | Importe máximo GTS |
| 189 | `GTSResponseToExceeding` | [GTSResponseToExceedingEnum](../Enums/GTSResponseToExceedingEnum.md) | Yes | GTS Response To Exceeding | Respuesta GTS al exceder |
| 190 | `ApplicationOfIFRS` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Application Of IFRS | Aplicación de NIIF |
| 191 | `StartingInFiscalYear` | Edm.Int32 | Yes | Starting In Fiscal Year | Inicio en el ejercicio |
| 192 | `ReportAccordingTo` | Edm.Int32 | Yes | Report According To | Informar según |
| 193 | `CopyOpenRowsToDelivery` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Copy Open Rows To Delivery | Copiar líneas abiertas a la entrega |
| 194 | `EnableApprovalProcedureInDI` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Approval Procedure In DI | Habilitar procedimiento de autorización en DI API |
| 195 | `EnableUpdateDocAfterApproval` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Update Document After Approval | Permitir actualizar documento después de autorizar |
| 196 | `EnableUpdateDraftDuringApproval` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Update Draft During Approval | Permitir actualizar borrador durante la autorización |
| 197 | `EnableAuthorizerUpdatePendingDraft` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Authorizer Update Pending Draft | Permitir al autorizador actualizar borradores pendientes |
| 198 | `IssuePrimarilyBy` | [IssuePrimarilyByEnum](../Enums/IssuePrimarilyByEnum.md) | Yes | Issue Primarily By | Emitir principalmente por |
| 199 | `IsRemoveUnpricedValue` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Remove Unpriced Value | Eliminar valor sin precio |
| 200 | `EnableAdvancedGLAccountDetermination` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Advanced G/L Account Determination | Habilitar determinación avanzada de cuentas de mayor |
| 201 | `CreateOnlineQuotation` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Create Online Quotation | Crear oferta en línea |
| 202 | `IsPrinterConnected` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Printer Connected | Impresora conectada |
| 203 | `EnableBranches` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Branches | Habilitar sucursales |
| 204 | `IEMandatoryValidation` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | IE Mandatory Validation | Validación obligatoria de I.E. |
| 205 | `EnablePaymentDueDates` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Payment Due Dates | Habilitar fechas de vencimiento de pago |
| 206 | `MaximumNumberOfDaysForDueDate` | Edm.Int32 | Yes | Maximum Number Of Days For Due Date | Días máximos para la fecha de vencimiento |
| 207 | `AliasName` | Edm.String | Yes | Alias Name | Alias |
| 208 | `EnableCentralizedIncomingPayments` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Centralized Incoming Payments | Habilitar pagos recibidos centralizados |
| 209 | `EnableCentralizedOutgoingPayments` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Centralized Outgoing Payments | Habilitar pagos efectuados centralizados |
| 210 | `TaxRateDetermination` | [TaxRateDeterminationEnum](../Enums/TaxRateDeterminationEnum.md) | Yes | Tax Rate Determination | Determinación de la tasa de impuesto |
| 211 | `BoletoFolderPath` | Edm.String | Yes | Boleto Folder Path | Ruta de carpeta de boletos |
| 212 | `AllowMultipleBAOnSamePeriod` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Allow Multiple BA On Same Period | Permitir varios acuerdos globales en el mismo período |
| 213 | `BlockMultipleBAOnSameAPDocument` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Block Multiple BA On Same AP Document | Bloquear varios acuerdos globales en el mismo documento de compras |
| 214 | `BlockMultipleBAOnSameARDocument` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Block Multiple BA On Same AR Document | Bloquear varios acuerdos globales en el mismo documento de ventas |
| 215 | `DisplayCancelDocInReport` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Display Cancel Document In Report | Mostrar documentos cancelados en informes |
| 216 | `MaxDaysForCancel` | Edm.Int32 | Yes | Max Days For Cancel | Días máximos para cancelar |
| 217 | `ReuseDocumentNum` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Reuse Document Number | Reutilizar número de documento |
| 218 | `ReuseNotaFiscalNum` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Reuse Nota Fiscal Number | Reutilizar número de Nota Fiscal |
| 219 | `AutoAddUoM` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Auto Add Uo M | Agregar unidad de medida automáticamente |
| 220 | `AutoAddPackage` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Auto Add Package | Agregar paquete automáticamente |
| 221 | `DisplayInactivePriceListInReports` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Display Inactive Price List In Reports | Mostrar listas de precios inactivas en informes |
| 222 | `DisplayInactivePriceListInDocuments` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Display Inactive Price List In Documents | Mostrar listas de precios inactivas en documentos |
| 223 | `DisplayInactivePriceListInSettings` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Display Inactive Price List In Settings | Mostrar listas de precios inactivas en configuración |
| 224 | `ApplyBaseInactiveStatusToSpecialPrices` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Apply Base Inactive Status To Special Prices | Aplicar estado inactivo base a precios especiales |
| 225 | `ApplyBaseInactiveStatusToPeriodVolumeDiscounts` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Apply Base Inactive Status To Period Volume Discounts | Aplicar estado inactivo base a descuentos por período y volumen |
| 226 | `ApplyBaseInactiveStatusToPriceLists` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Apply Base Inactive Status To Price Lists | Aplicar estado inactivo base a listas de precios |
| 227 | `PriceProceedMethod` | [PriceProceedMethodEnum](../Enums/PriceProceedMethodEnum.md) | Yes | Price Proceed Method | Método de procesamiento de precios |
| 228 | `RemoveUpdatePricesBasedOnNonStandardPriceLists` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Remove Update Prices Based On Non Standard Price Lists | Quitar actualización de precios basada en listas no estándar |
| 229 | `SirenNo` | Edm.String | Yes | Siren Number | Número SIREN (Francia) |
| 230 | `InstitutionCode` | Edm.String | Yes | Institution Code | Código de institución |
| 231 | `SetResourcesWarehouses` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Set Resources Warehouses | Asignar almacenes a recursos |
| 232 | `BlockStockNegativeQuantity` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Block Stock Negative Quantity | Bloquear cantidad negativa de stock |
| 233 | `UseParentWIPInComponents` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Use Parent WIP In Components | Usar WIP del padre en componentes |
| 234 | `EnableUpdateBAPriceAndPlannedAmount` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Update BA Price And Planned Amount | Permitir actualizar precio e importe planificado del acuerdo global |
| 235 | `AutoAssignOnlyValidAPBA` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Auto Assign Only Valid APBA | Asignar automáticamente solo acuerdos globales de compras válidos |
| 236 | `AutoAssignOnlyValidARBA` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Auto Assign Only Valid ARBA | Asignar automáticamente solo acuerdos globales de ventas válidos |
| 237 | `ActionWhenDeviateFromBAForPO` | [BADivationAlertLevelEnum](../Enums/BADivationAlertLevelEnum.md) | Yes | Action When Deviate From BA For PO | Acción si se desvía del acuerdo global (pedido de compra) |
| 238 | `ActionWhenDeviateFromBAForGRPO` | [BADivationAlertLevelEnum](../Enums/BADivationAlertLevelEnum.md) | Yes | Action When Deviate From BA For GRPO | Acción si se desvía del acuerdo global (pedido de entrada) |
| 239 | `ActionWhenDeviateFromBAForAccounting` | [BADivationAlertLevelEnum](../Enums/BADivationAlertLevelEnum.md) | Yes | Action When Deviate From BA For Accounting | Acción si se desvía del acuerdo global (contabilidad) |
| 240 | `Series` | Edm.Int32 | Yes | Series | Serie de numeración |
| 241 | `Account` | Edm.String | Yes | Account | Cuenta |
| 242 | `EnableMultipleSchedulings` | Edm.String | Yes | Enable Multiple Schedulings | Habilitar programaciones múltiples |
| 243 | `DisplayBatchQtyUoMBy` | [DisplayBatchQtyUoMByEnum](../Enums/DisplayBatchQtyUoMByEnum.md) | Yes | Display Batch Quantity Uo M By | Mostrar cantidad de lote por unidad de medida |
| 244 | `AllowInBoundPostingWithZeroPrice` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Allow In Bound Posting With Zero Price | Permitir contabilización de entradas con precio cero |
| 245 | `InventoryPostingHighlightVariance` | Edm.Double | Yes | Inventory Posting Highlight Variance | Resaltar desviación en contabilización de inventario |
| 246 | `InventoryPostingReleaseOnlySerialAndBatch` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Inventory Posting Release Only Serial And Batch | Liberar solo series y lotes en contabilización de inventario |
| 247 | `InventoryCountingHighlightVariance` | Edm.Double | Yes | Inventory Counting Highlight Variance | Resaltar desviación del recuento |
| 248 | `InventoryCountingHighlightMaxVariance` | Edm.Double | Yes | Inventory Counting Highlight Max Variance | Resaltar desviación máxima del recuento |
| 249 | `InventoryCountingHighlightCountersDifference` | Edm.Double | Yes | Inventory Counting Highlight Counters Difference | Resaltar diferencia entre contadores |
| 250 | `CopySingleCounterToIndividualCounter` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Copy Single Counter To Individual Counter | Copiar contador único a contador individual |
| 251 | `CloseCountedRowsWithZeroDifference` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Close Counted Rows With Zero Difference | Cerrar líneas contadas sin diferencia |
| 252 | `CloseCountedRowsWithoutConfirmation` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Close Counted Rows Without Confirmation | Cerrar líneas contadas sin confirmación |
| 253 | `CalculateInWhseQtyBasedOnPostingDate` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Calculate In Whse Quantity Based On Posting Date | Calcular cantidad en almacén según fecha de contabilización |
| 254 | `RefreshInWhseQtyInDI` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Refresh In Whse Quantity In DI | Actualizar cantidad en almacén en DI |
| 255 | `SEPACreditorID` | Edm.String | Yes | SEPA Creditor ID | ID de acreedor SEPA |
| 256 | `DataOwnershipManageBy` | [BoDataOwnershipManageMethodEnum](../Enums/BoDataOwnershipManageMethodEnum.md) | Yes | Data Ownership Manage By | Propiedad de datos gestionada por |
| 257 | `AllowBPWithNoOwner` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Allow Business Partner With Number Owner | Permitir socios de negocios sin propietario |
| 258 | `EnableSeparatePriceMode` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable Separate Price Mode | Habilitar modo de precio separado |
| 259 | `EnableExternalTax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Enable External Tax | Habilitar impuestos externos |
| 260 | `NumberOfCharInMonth` | Edm.Int32 | Yes | Number Of Char In Month | Cantidad de caracteres del mes |
| 261 | `SalesLnWTax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Sales Ln W Tax | Retención en línea de ventas |
| 262 | `SalesPostPaymentCategoryLnWTax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Sales Post Payment Category Ln W Tax | Categoría de pago posterior con retención en línea (ventas) |
| 263 | `SalesApplyExhRatesLnWTax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Sales Apply Exh Rates Ln W Tax | Aplicar tipo de cambio en línea con retención (ventas) |
| 264 | `PurchaseLnWTax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Purchase Ln W Tax | Retención en línea de compras |
| 265 | `PurchasePostPaymentCategoryLnWTax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Purchase Post Payment Category Ln W Tax | Categoría de pago posterior con retención en línea (compras) |
| 266 | `PurchaseApplyExhRatesLnWTaxWX` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Purchase Apply Exh Rates Ln W Tax WX | Aplicar tipo de cambio en línea con retención (compras) |
| 267 | `UseDefaultPriceList` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Use Default Price List | Usar lista de precios predeterminada |
| 268 | `DefaultCustomerPriceList` | Edm.Int32 | Yes | Default Customer Price List | Lista de precios predeterminada de clientes |
| 269 | `DefaultVendorPriceList` | Edm.Int32 | Yes | Default Vendor Price List | Lista de precios predeterminada de proveedores |
| 270 | `EORINumber` | Edm.String | Yes | EORI Number | Número EORI |
| 271 | `CopyAttachmentsFromBaseToTarget` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Copy Attachments From Base To Target | Copiar anexos del documento base al destino |
| 272 | `CopyAttachmentsFromBOM` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Copy Attachments From BOM | Copiar anexos de la lista de materiales |
| 273 | `DontOverwriteAtcWithSameName` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Dont Overwrite Atc With Same Name | No sobrescribir anexos con el mismo nombre |
| 274 | `AttachmentEntryForFileStorage` | Edm.Int32 | Yes | Attachment Entry For File Storage | Entrada de anexo para almacenamiento de archivos |
| 275 | `DontDuplicatwAttachment` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Dont Duplicatw Attachment | No duplicar anexos |
| 276 | `ExtendedAdminInfo` | [ExtendedAdminInfo](../Tipos-Complejos/ExtendedAdminInfo.md) | Yes | Extended Admin Information | Información de administración ampliada |
| 277 | `ElectronicReportInfo` | [ElectronicReportInfo](../Tipos-Complejos/ElectronicReportInfo.md) | Yes | Electronic Report Information | Información de informe electrónico |

## Used by (service operations)

- [`CompanyService_GetAdminInfo`](../Servicios/CompanyService.md#companyservice_getadmininfo)
- [`CompanyService_UpdateAdminInfo`](../Servicios/CompanyService.md#companyservice_updateadmininfo)
