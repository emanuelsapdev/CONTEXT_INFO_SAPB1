# PeriodCategory — Categoría de períodos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `PeriodCategory`
- **Descripción (ES):** Categoría de períodos
- **Description (EN):** Period Category

- **Properties:** 128

## Properties (128)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsoluteEntry` | Edm.Int32 | Yes | Absolute Entry | Entrada absoluta (ID interno) |
| 2 | `BeginningofFinancialYear` | Edm.DateTimeOffset | Yes | Beginningof Financial Year | Inicio del ejercicio |
| 3 | `PeriodCategoryProperty` | Edm.String | Yes | Period Category Property | Propiedad de categoría de período |
| 4 | `SubPeriodType` | [BoSubPeriodTypeEnum](../Enums/BoSubPeriodTypeEnum.md) | Yes | Sub Period Type | Tipo de subperíodo |
| 5 | `NumberOfPeriods` | Edm.Int32 | Yes | Number Of Periods | Cantidad de períodos |
| 6 | `PeriodName` | Edm.String | Yes | Period Name | Nombre del período |
| 7 | `DebitorsFollowUpAccount` | Edm.String | Yes | Debitors Follow Up Account | Cuenta de seguimiento de deudores |
| 8 | `AccountforOutgoingChecks` | Edm.String | Yes | Accountfor Outgoing Checks | Cuenta para cheques emitidos |
| 9 | `AccountforCashReceipt` | Edm.String | Yes | Accountfor Cash Receipt | Cuenta para cobros en efectivo |
| 10 | `CustomersDeductionatSource` | Edm.String | Yes | Customers Deductionat Source | Retención en la fuente de clientes |
| 11 | `CommissionAccountDefault` | Edm.String | Yes | Commission Account Default | Cuenta de comisión predeterminada |
| 12 | `PurchaseTax` | Edm.String | Yes | Purchase Tax | Impuesto de compras |
| 13 | `ForeignAccountsReceivables` | Edm.String | Yes | Foreign Accounts Receivables | Cuentas por cobrar del exterior |
| 14 | `CreditorsFollowUpAccount` | Edm.String | Yes | Creditors Follow Up Account | Cuenta de seguimiento de acreedores |
| 15 | `OutgoingChecksAccount` | Edm.String | Yes | Outgoing Checks Account | Cuenta de cheques emitidos |
| 16 | `OutgoingCashAccount` | Edm.String | Yes | Outgoing Cash Account | Cuenta de caja para pagos |
| 17 | `AccountforCreditMemoPayme` | Edm.String | Yes | Accountfor Credit Memo Payme | Cuenta para pagos de notas de crédito |
| 18 | `InputTaxAccount` | Edm.String | Yes | Input Tax Account | Cuenta de impuesto soportado |
| 19 | `TaxDefinition` | Edm.String | Yes | Tax Definition | Definición de impuestos |
| 20 | `WithholodingTax` | Edm.String | Yes | Withholoding Tax | Retención de impuestos |
| 21 | `OpeningBalancesAccount` | Edm.String | Yes | Opening Balances Account | Cuenta de saldos iniciales |
| 22 | `DefaultSaleAccount` | Edm.String | Yes | Default Sale Account | Cuenta de ventas predeterminada |
| 23 | `TaxExemptRevenuesDefault` | Edm.String | Yes | Tax Exempt Revenues Default | Ingresos exentos predeterminados |
| 24 | `ExpenseAccountDefault` | Edm.String | Yes | Expense Account Default | Cuenta de gastos predeterminada |
| 25 | `RevenuesAccountForeign` | Edm.String | Yes | Revenues Account Foreign | Cuenta de ingresos (exterior) |
| 26 | `SalesRevenueEU` | Edm.String | Yes | Sales Revenue EU | Ingresos por ventas UE |
| 27 | `ExpensesAccountForeign` | Edm.String | Yes | Expenses Account Foreign | Cuenta de gastos (exterior) |
| 28 | `RateDifferencesDefaultAcc` | Edm.String | Yes | Rate Differences Default Account | Cuenta predeterminada de diferencias de cambio |
| 29 | `DecreaseGLAcc` | Edm.String | Yes | Decrease G/L Account | Cuenta de mayor de disminución |
| 30 | `ReconciliationDifference` | Edm.String | Yes | Reconciliation Difference | Diferencia de conciliación |
| 31 | `AcountforOpeningWHBalance` | Edm.String | Yes | Acountfor Opening Warehouse Balance | Cuenta para saldo inicial de almacén |
| 32 | `APCashDiscountAccount` | Edm.String | Yes | AP Cash Discount Account | Cuenta de descuento por pronto pago (compras) |
| 33 | `APLossCashDiscountAccount` | Edm.String | Yes | AP Loss Cash Discount Account | Cuenta de pérdida por descuento por pronto pago (compras) |
| 34 | `APLossRealizedExchangeDif` | Edm.String | Yes | AP Loss Realized Exchange Dif | Pérdida realizada por diferencia de cambio (compras) |
| 35 | `ARCashDiscountAccount` | Edm.String | Yes | AR Cash Discount Account | Cuenta de descuento por pronto pago (ventas) |
| 36 | `ARLossRealizedExchangeDi` | Edm.String | Yes | AR Loss Realized Exchange Di | Pérdida realizada por diferencia de cambio (ventas) |
| 37 | `RoundingAccount` | Edm.String | Yes | Rounding Account | Cuenta de redondeo |
| 38 | `APGainRealizedExchngeDif` | Edm.String | Yes | AP Gain Realized Exchnge Dif | Ganancia realizada por diferencia de cambio (compras) |
| 39 | `ARGainRealizedExchngeDif` | Edm.String | Yes | AR Gain Realized Exchnge Dif | Ganancia realizada por diferencia de cambio (ventas) |
| 40 | `IncreaseGLAccount` | Edm.String | Yes | Increase G/L Account | Cuenta de mayor de aumento |
| 41 | `SalesReturns` | Edm.String | Yes | Sales Returns | Devoluciones de ventas |
| 42 | `CostOfGoodsSold` | Edm.String | Yes | Cost Of Goods Sold | Costo de ventas |
| 43 | `AllocationAcc` | Edm.String | Yes | Allocation Account | Cuenta de asignación |
| 44 | `VarianceAcc` | Edm.String | Yes | Variance Account | Cuenta de desviaciones |
| 45 | `PriceDifferenceAccount` | Edm.String | Yes | Price Difference Account | Cuenta de diferencias de precio |
| 46 | `CustomerDownPaymentsAccount` | Edm.String | Yes | Customer Down Payments Account | Cuenta de anticipos de clientes |
| 47 | `VendorDownPaymentsAccount` | Edm.String | Yes | Vendor Down Payments Account | Cuenta de anticipos a proveedores |
| 48 | `BillofExchangeAccountsRece` | Edm.String | Yes | Billof Exchange Accounts Rece | Cuenta de letras de cambio por cobrar |
| 49 | `CustBillofExchangeonC` | Edm.String | Yes | Cust Billof Exchangeon C | Letras de cambio de clientes en cobranza |
| 50 | `CustomerBillofExchangePres` | Edm.String | Yes | Customer Billof Exchange Pres | Letras de cambio de clientes presentadas |
| 51 | `CustomerBillofExchngeDisc` | Edm.String | Yes | Customer Billof Exchnge Disc | Letras de cambio de clientes descontadas |
| 52 | `CustomerUnpaidBoE` | Edm.String | Yes | Customer Unpaid Bo E | Letras de cambio impagas de clientes |
| 53 | `BoEAccountsPayable` | Edm.String | Yes | Bo E Accounts Payable | Letras de cambio por pagar |
| 54 | `BoEAccountsPayable2` | Edm.String | Yes | Bo E Accounts Payable 2 | Letras de cambio por pagar 2 |
| 55 | `CustomerDoubtfulDebtsAcct` | Edm.String | Yes | Customer Doubtful Debts Account | Cuenta de deudas dudosas de clientes |
| 56 | `VendorDoubtfulDebtsAcct` | Edm.String | Yes | Vendor Doubtful Debts Account | Cuenta de deudas dudosas de proveedores |
| 57 | `PurchaseAccount` | Edm.String | Yes | Purchase Account | Cuenta de compras |
| 58 | `PurchaseReturnAccount` | Edm.String | Yes | Purchase Return Account | Cuenta de devoluciones de compras |
| 59 | `PurchaseOffsetAccount` | Edm.String | Yes | Purchase Offset Account | Contracuenta de compras |
| 60 | `EOYControlAccount` | Edm.String | Yes | EOY Control Account | Cuenta asociada de fin de año |
| 61 | `ExchangeRateDifferencesAcct` | Edm.String | Yes | Exchange Rate Differences Account | Cuenta de diferencias de cambio |
| 62 | `GoodsClearingAcc` | Edm.String | Yes | Goods Clearing Account | Cuenta de compensación de mercancías |
| 63 | `ExpenseClearingAccount` | Edm.String | Yes | Expense Clearing Account | Cuenta de compensación de gastos |
| 64 | `ExpenseOffsetAccount` | Edm.String | Yes | Expense Offset Account | Contracuenta de gastos |
| 65 | `CostofSaleRevaluationAcct` | Edm.String | Yes | Costof Sale Revaluation Account | Cuenta de revalorización del costo de ventas |
| 66 | `RepomoAccount` | Edm.String | Yes | Repomo Account | Cuenta REPOMO (México) |
| 67 | `WIPMaterialVarianceAccount` | Edm.String | Yes | WIP Material Variance Account | Cuenta de desviación de materiales WIP |
| 68 | `DownPaymentVATAcctSale` | Edm.String | Yes | Down Payment VAT Account Sale | Cuenta de IVA de anticipos (ventas) |
| 69 | `DownPaymentVATAcctPurch` | Edm.String | Yes | Down Payment VAT Account Purch | Cuenta de IVA de anticipos (compras) |
| 70 | `DownPaymentSClearingAcct` | Edm.String | Yes | Down Payment S Clearing Account | Cuenta de compensación de anticipos (ventas) |
| 71 | `DownPaymentPClearingAcct` | Edm.String | Yes | Down Payment P Clearing Account | Cuenta de compensación de anticipos (compras) |
| 72 | `ExpenseVarianceAccount` | Edm.String | Yes | Expense Variance Account | Cuenta de desviación de gastos |
| 73 | `CostofSaleRevOffsetAcct` | Edm.String | Yes | Costof Sale Rev Offset Account | Contracuenta de revalorización del costo de ventas |
| 74 | `EUExpenseAccount` | Edm.String | Yes | EU Expense Account | Cuenta de gastos UE |
| 75 | `StockAccount` | Edm.String | Yes | Stock Account | Cuenta de stock |
| 76 | `InventoryOffsetIncrease` | Edm.String | Yes | Inventory Offset Increase | Contracuenta de aumento de inventario |
| 77 | `InventoryOffsetDecrease` | Edm.String | Yes | Inventory Offset Decrease | Contracuenta de disminución de inventario |
| 78 | `VendorAssetsAccount` | Edm.String | Yes | Vendor Assets Account | Cuenta de activos de proveedores |
| 79 | `StockRevaluationAccount` | Edm.String | Yes | Stock Revaluation Account | Cuenta de revalorización de stock |
| 80 | `StockRevaluationOffsetAcct` | Edm.String | Yes | Stock Revaluation Offset Account | Contracuenta de revalorización de stock |
| 81 | `WIPMaterialAccount` | Edm.String | Yes | WIP Material Account | Cuenta de materiales WIP |
| 82 | `InvoicePaymentBP` | Edm.String | Yes | Invoice Payment Business Partner | Socio de negocios del pago de factura |
| 83 | `GLRevaluationOffsetAccount` | Edm.String | Yes | G/L Revaluation Offset Account | Contracuenta de revalorización de mayor |
| 84 | `OverpaymentsAPAccount` | Edm.String | Yes | Overpayments AP Account | Cuenta de pagos en exceso (compras) |
| 85 | `UnderpaymentsAPAccount` | Edm.String | Yes | Underpayments AP Account | Cuenta de pagos de menos (compras) |
| 86 | `OverpaymentsARAccount` | Edm.String | Yes | Overpayments AR Account | Cuenta de pagos en exceso (ventas) |
| 87 | `UnderpaymentsARAccount` | Edm.String | Yes | Underpayments AR Account | Cuenta de pagos de menos (ventas) |
| 88 | `PurchaseCreditAcc` | Edm.String | Yes | Purchase Credit Account | Cuenta de haber de compras |
| 89 | `EUPurchaseCreditAcc` | Edm.String | Yes | EU Purchase Credit Account | Cuenta de haber de compras UE |
| 90 | `ForeignPurchaseCreditAcc` | Edm.String | Yes | Foreign Purchase Credit Account | Cuenta de haber de compras del exterior |
| 91 | `SalesCreditAcc` | Edm.String | Yes | Sales Credit Account | Cuenta de haber de ventas |
| 92 | `SalesCreditEUAcc` | Edm.String | Yes | Sales Credit EU Account | Cuenta de haber de ventas UE |
| 93 | `ExemptedCredits` | Edm.String | Yes | Exempted Credits | Créditos exentos |
| 94 | `SalesCreditForeignAcc` | Edm.String | Yes | Sales Credit Foreign Account | Cuenta de haber de ventas del exterior |
| 95 | `FromPostingDate` | Edm.DateTimeOffset | Yes | From Posting Date | Fecha de contabilización desde |
| 96 | `ToPostingDate` | Edm.DateTimeOffset | Yes | To Posting Date | Fecha de contabilización hasta |
| 97 | `FromDueDate` | Edm.DateTimeOffset | Yes | From Due Date | Fecha de vencimiento desde |
| 98 | `ToDueDate` | Edm.DateTimeOffset | Yes | To Due Date | Fecha de vencimiento hasta |
| 99 | `FromDocumentDate` | Edm.DateTimeOffset | Yes | From Document Date | Fecha del documento desde |
| 100 | `ToDocumentDate` | Edm.DateTimeOffset | Yes | To Document Date | Fecha del documento hasta |
| 101 | `OutgoingTaxAccount` | Edm.String | Yes | Outgoing Tax Account | Cuenta de impuesto repercutido |
| 102 | `NegativeInventoryAdjustmentAccount` | Edm.String | Yes | Negative Inventory Adjustment Account | Cuenta de ajuste de inventario negativo |
| 103 | `FinancialYear` | Edm.Int32 | Yes | Financial Year | Ejercicio |
| 104 | `SelfInvoiceRevenueAccount` | Edm.String | Yes | Self Invoice Revenue Account | Cuenta de ingresos de autofactura |
| 105 | `SelfInvoiceExpenseAccount` | Edm.String | Yes | Self Invoice Expense Account | Cuenta de gastos de autofactura |
| 106 | `StockInTransitAccount` | Edm.String | Yes | Stock In Transit Account | Cuenta de stock en tránsito |
| 107 | `SalesDownPaymentInterimAccount` | Edm.String | Yes | Sales Down Payment Interim Account | Cuenta transitoria de anticipos de ventas |
| 108 | `PurchaseDownPaymentInterimAccount` | Edm.String | Yes | Purchase Down Payment Interim Account | Cuenta transitoria de anticipos de compras |
| 109 | `EUAccountsReceivable` | Edm.String | Yes | EU Accounts Receivable | Cuentas por cobrar UE |
| 110 | `EUAccountsPayable` | Edm.String | Yes | EU Accounts Payable | Cuentas por pagar UE |
| 111 | `WipOffsetProfitAndLossAccount` | Edm.String | Yes | Wip Offset Profit And Loss Account | Contracuenta WIP de pérdidas y ganancias |
| 112 | `InventoryOffsetProfitAndLossAccount` | Edm.String | Yes | Inventory Offset Profit And Loss Account | Contracuenta de inventario de pérdidas y ganancias |
| 113 | `DunningInterestAccount` | Edm.String | Yes | Dunning Interest Account | Cuenta de intereses de reclamación |
| 114 | `DunningFeeAccount` | Edm.String | Yes | Dunning Fee Account | Cuenta de cargos por reclamación |
| 115 | `ARGainRealizedConversionDiff` | Edm.String | Yes | AR Gain Realized Conversion Diff | Ganancia realizada por diferencia de conversión (ventas) |
| 116 | `ARLossRealizedConversionDiff` | Edm.String | Yes | AR Loss Realized Conversion Diff | Pérdida realizada por diferencia de conversión (ventas) |
| 117 | `APGainRealizedConversionDiff` | Edm.String | Yes | AP Gain Realized Conversion Diff | Ganancia realizada por diferencia de conversión (compras) |
| 118 | `APLossRealizedConversionDiff` | Edm.String | Yes | AP Loss Realized Conversion Diff | Pérdida realizada por diferencia de conversión (compras) |
| 119 | `GLGainRealizedConversionDiff` | Edm.String | Yes | G/L Gain Realized Conversion Diff | Ganancia realizada por diferencia de conversión (mayor) |
| 120 | `GLLossRealizedConversionDiff` | Edm.String | Yes | G/L Loss Realized Conversion Diff | Pérdida realizada por diferencia de conversión (mayor) |
| 121 | `ARExRateInterim` | Edm.String | Yes | AR Ex Rate Interim | Cuenta transitoria de tipo de cambio (ventas) |
| 122 | `APExRateInterim` | Edm.String | Yes | AP Ex Rate Interim | Cuenta transitoria de tipo de cambio (compras) |
| 123 | `ARCashDiscountInterim` | Edm.String | Yes | AR Cash Discount Interim | Cuenta transitoria de descuento por pronto pago (ventas) |
| 124 | `APCashDiscountInterim` | Edm.String | Yes | AP Cash Discount Interim | Cuenta transitoria de descuento por pronto pago (compras) |
| 125 | `SalesInterimAcctLnWTax` | Edm.String | Yes | Sales Interim Account Ln W Tax | Cuenta transitoria de ventas con retención en línea |
| 126 | `PurchaseInterimAcctLnWTax` | Edm.String | Yes | Purchase Interim Account Ln W Tax | Cuenta transitoria de compras con retención en línea |
| 127 | `ExhRatesDiffAcctLnWTax` | Edm.String | Yes | Exh Rates Diff Account Ln W Tax | Cuenta de diferencias de cambio con retención |
| 128 | `WIPMappingCollection` | Collection([WIPMapping](../Tipos-Complejos/WIPMapping.md)) | Yes | WIP Mapping Collection | Colección de mapeo WIP |

## Used by (service operations)

- [`CompanyService_CreatePeriod`](../Servicios/CompanyService.md#companyservice_createperiod)
- [`CompanyService_CreatePeriodWithFinanceParams`](../Servicios/CompanyService.md#companyservice_createperiodwithfinanceparams)
- [`CompanyService_GetPeriod`](../Servicios/CompanyService.md#companyservice_getperiod)
- [`CompanyService_UpdatePeriod`](../Servicios/CompanyService.md#companyservice_updateperiod)
