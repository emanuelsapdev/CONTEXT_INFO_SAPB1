# AACP - Periods Category-Log

- **Tabla:** AACP
- **Descripción:** Periods Category-Log
- **Cantidad de campos:** 183
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AACP.html

## Campos (183)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - | 0 |  |
| 2 | `PeriodCat` | Period Category | nVarChar | 10 | - |  |  |
| 3 | `FinancYear` | Beginning of Financial Year | Date | 8 | - |  |  |
| 4 | `Year` | Financial Year | Int | 6 | - |  |  |
| 5 | `PeriodName` | Period Name | nVarChar | 20 | - |  |  |
| 6 | `SubType` | Sub-Period Type | VarChar | 1 | - | Y | `Y` = Year<br>`Q` = Quarters<br>`M` = Months<br>`D` = Days |
| 7 | `PeriodNum` | Number of Periods | Int | 11 | - |  |  |
| 8 | `F_RefDate` | Posting Date From | Date | 8 | - |  |  |
| 9 | `T_RefDate` | Posting Date To | Date | 8 | - |  |  |
| 10 | `F_DueDate` | Due Date From | Date | 8 | - |  |  |
| 11 | `T_DueDate` | Due Date To | Date | 8 | - |  |  |
| 12 | `F_TaxDate` | Document Date From | Date | 8 | - |  |  |
| 13 | `T_TaxDate` | Document Date To | Date | 8 | - |  |  |
| 14 | `LogInstanc` | Log Instance | Int | 11 | - |  |  |
| 15 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 16 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 17 | `LinkAct_1` | Domestic Accounts Receivable | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 18 | `LinkAct_2` | Checks Received | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 19 | `LinkAct_3` | Cash on Hand | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 20 | `LinkAct_4` | Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 21 | `LinkAct_5` | Sales Tax Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 22 | `LinkAct_6` | Customer's Deduction at Source | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 23 | `ComissAct` | Credit Card Deposit Fee | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 24 | `LinkAct_8` | Purchase Tax | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 25 | `LinkAct_9` | Foreign Accounts Receivable | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 26 | `LinkAct_10` | Domestic Accounts Payable | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 27 | `LinkAct_11` | Foreign Accounts Payable | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 28 | `LinkAct_12` | Bank Transfer | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 29 | `LinkAct_13` | Tax to Pay to | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 30 | `LinkAct_14` | Tax Definition | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 31 | `LinkAct_15` | Equipment and Assets | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 32 | `LinkAct_16` | Withholding Tax | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 33 | `LinkAct_17` | Advances on Corp. Income Tax | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 34 | `LinkAct_18` | Opening Balance Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 35 | `DfltIncom` | Revenue Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 36 | `ExmptIncom` | Tax Exempt Revenue Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 37 | `DfltExpn` | Expense Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 38 | `ForgnIncm` | Revenue Account - Foreign | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 39 | `ECIncome` | Sales Revenue - EU | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 40 | `ForgnExpn` | Expense Account - Foreign | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 41 | `DfltRateDi` | Ex. Rate Diff. in All Currency | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 42 | `DecresGlAc` | G/L Decrease Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 43 | `LinkAct_27` | Automatic Reconciliation Diff. | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 44 | `DftStockOB` | Account for Opening Whse Bal. | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 45 | `LinkAct_19` | Cash Discount | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 46 | `LinkAct_20` | Cash Discount Clearing | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 47 | `LinkAct_21` | Realized Exchange Diff. Loss | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 48 | `LinkAct_22` | Cash Discount | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 49 | `LinkAct_23` | Realized Exchange Diff. Loss | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 50 | `LinkAct_24` | Rounding Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 51 | `LinkAct_25` | Realized Exchange Diff. Gain | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 52 | `LinkAct_26` | Realized Exchange Diff. Gain | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 53 | `IncresGlAc` | G/L Increase Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 54 | `RturnngAct` | Sales Returns Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 55 | `COGM_Act` | Cost of Goods Sold Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 56 | `AlocCstAct` | Allocation Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 57 | `VariancAct` | Variance Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 58 | `PricDifAct` | Price Difference Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 59 | `CDownPymnt` | Customer Down Payment Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 60 | `VDownPymnt` | Vendor Down Payment Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 61 | `CBoERcvble` | BoE Accounts Receivable | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 62 | `CBoEOnClct` | Bill of Exchange on Collection | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 63 | `CBoEPresnt` | Bill of Exchange Presentation | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 64 | `CBoEDiscnt` | Bill of Exchange Discounted | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 65 | `CUnpaidBoE` | Unpaid Bill of Exchange | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 66 | `VBoEPayble` | BoE Accounts Payable | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 67 | `VAsstBoEPy` | BoE Accounts Payable | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 68 | `COpenDebts` | Customer Doubtful Debts Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 69 | `VOpenDebts` | Vendor Doubtful Debts Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 70 | `PurchseAct` | Purchase Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 71 | `PaReturnAc` | Purchase Return Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 72 | `PaOffsetAc` | Purchase Offset Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 73 | `LinkAct_28` | Period-End Closing Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 74 | `ExDiffAct` | Exchange Rate Difference Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 75 | `BalanceAct` | Goods Clearing Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 76 | `BnkChgAct` | Bank Charge Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 77 | `LinkAct_29` | Other Receivable | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 78 | `LinkAct_30` | Other Payable | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 79 | `IncmAcct` | Def. Inv. Reval. Revenue Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 80 | `ExpnAcct` | Def. Inventory Reval. Expense | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 81 | `VatRevAct` | VAT in Revenue Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 82 | `ExpClrAct` | Expense Account for Tax | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 83 | `ExpOfstAct` | Expense Offset Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 84 | `CostRevAct` | COGS Revaluation Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 85 | `RepomoAct` | REPOMO Revaluation Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 86 | `WipVarAcct` | WIP Inventory Variance Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 87 | `SaleVatOff` | Down Payment Tax Offset Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 88 | `PurcVatOff` | Down Payment Tax Offset Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 89 | `DpmSalAct` | Payment Advances | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 90 | `DpmPurAct` | Payment Advances | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 91 | `ExpVarAct` | Expense and Inventory Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 92 | `CostOffAct` | Cost of Sale Rev. Offset Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 93 | `ECExepnses` | Expense Account - EU | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 94 | `StockAct` | Inventory Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 95 | `DflInPrcss` | Default for Stk Itm in Process | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 96 | `DfltInCstm` | Default for Stock Item in Cust | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 97 | `DfltProfit` | Inventory Offset - Incr. Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 98 | `DfltLoss` | Inventory Offset - Decr. Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 99 | `VAssets` | Vendor Asset Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 100 | `StockRvAct` | Inventory Revaluation Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 101 | `StkRvOfAct` | Invent Revaluation Offset Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 102 | `WipAcct` | WIP Inventory Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 103 | `DfltCard` | Invoice and Payment BP | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 104 | `ShpdGdsAct` | Shipped Goods Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 105 | `GlRvOffAct` | G/L Revaluation Offset Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 106 | `OverpayAP` | Overpayment A/P Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 107 | `UndrpayAP` | Underpayment A/P Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 108 | `OverpayAR` | Overpayment A/R Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 109 | `UndrpayAR` | Underpayment A/R Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 110 | `ARCMAct` | Sales Credit Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 111 | `ARCMExpAct` | Tax Exempt Credit Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 112 | `ARCMFrnAct` | Sales Credit Account - Foreign | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 113 | `ARCMEUAct` | Sales Credit Acct - EU | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 114 | `APCMAct` | Purchase Credit Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 115 | `APCMFrnAct` | Purchase Credit Acct - Foreign | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 116 | `APCMEUAct` | Purchase Credit Account - EU | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 117 | `NegStckAct` | Negative Inventory Adj. Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 118 | `StkInTnAct` | Stock In Transit Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 119 | `GLGainXdif` | Realized Exchange Diff. Gain | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 120 | `GLLossXdif` | Realized Exchange Diff. Loss | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 121 | `AmountDiff` | Amount Differences | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 122 | `SlfInvIncm` | Self Invoice Revenue Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 123 | `SlfInvExpn` | Self Invoice Expense Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 124 | `OnHoldAct` | Capital Goods On Hold Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 125 | `PlaAct` | PLA | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 126 | `ICClrAct` | Incoming CENVAT Clearing Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 127 | `OCClrAct` | Outgoing CENVAT Clearing Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 128 | `PurBalAct` | Purchase Balance Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 129 | `WhICenAct` | Incoming CENVAT Account (WH) | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 130 | `WhOCenAct` | Outgoing CENVAT Account (WH) | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 131 | `SalDpmInt` | A/R DP Interim | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 132 | `PurDpmInt` | A/P DP Interim | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 133 | `ExrateOnDt` | Ex Rate on Def Tax Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 134 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 135 | `EURecvAct` | EU Accounts Receivable | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 136 | `EUPayAct` | EU Accounts Payable | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 137 | `WipOffset` | WIP Offset P&L Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 138 | `StockOffst` | Inventory Offset P&L Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 139 | `DunIntrst` | Dunning Interest | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 140 | `DunFee` | Dunning Fee | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 141 | `SnapShotId` | Snapshot ID | Int | 11 | - | 0 |  |
| 142 | `TDSInterst` | TDS Interest Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 143 | `TDSCharges` | TDS Other Charges Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 144 | `SrvTaxClr` | Service Tax Clearing Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 145 | `ARConDiffG` | Realized Conversion Diff. Gain | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 146 | `ARConDiffL` | Realized Conversion Diff. Loss | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 147 | `APConDiffG` | Realized Conversion Diff. Gain | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 148 | `APConDiffL` | Realized Conversion Diff. Loss | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 149 | `GLConDiffG` | Realized Conversion Diff. Gain | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 150 | `GLConDiffL` | Realized Conversion Diff. Loss | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 151 | `FreeChrgSA` | Free of Charge Sales Account | nVarChar | 15 | - |  |  |
| 152 | `FreeChrgPU` | Free of Charge Purchase Account | nVarChar | 15 | - |  |  |
| 153 | `TDSFee` | TDS Fee Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 154 | `ResRevenue` | Revenue Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 155 | `ResExpense` | Expense Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 156 | `ResSalesCr` | Sales Credit Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 157 | `ResPurchCr` | Purchase Credit Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 158 | `ResNotInv` | Res. Received Not Inv. Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 159 | `ResStdExp1` | Std Cost Expense 1 | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 160 | `ResStdExp2` | Std Cost Expense 2 | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 161 | `ResStdExp3` | Std Cost Expense 3 | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 162 | `ResStdExp4` | Std Cost Expense 4 | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 163 | `ResStdExp5` | Std Cost Expense 5 | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 164 | `ResStdExp6` | Std Cost Expense 6 | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 165 | `ResStdExp7` | Std Cost Expense 7 | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 166 | `ResStdExp8` | Std Cost Expense 8 | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 167 | `ResStdExp9` | Std Cost Expense 9 | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 168 | `ResStdEx10` | Std Cost Expense 10 | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 169 | `ResWipAct` | Resource WIP Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 170 | `ResScrapAc` | Scrap Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 171 | `WipOffPlAc` | WIP Offset P&L Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 172 | `ResOffPlAc` | Resource Offset P&L Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 173 | `ERDInARAct` | Exchange Rate Interim Sales Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 174 | `ERDInAPAct` | Exchange Rate Interim Purchase Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 175 | `CSDInARAct` | Cash Discount Interim Sales Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 176 | `CSDInAPAct` | Cash Discount Interim Purchase Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 177 | `GSTInAct` | GST Input Interim Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 178 | `GSTInterst` | GST Interest Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 179 | `GSTCharges` | GST Other Charges Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 180 | `GSTFee` | GST Fee Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 181 | `WTInARAct` | Interim Account for Tax | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 182 | `WTInAPAct` | Interim Account for Tax | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 183 | `WTExDifAct` | Withholding Tax Exchange Rate Diff. Account | nVarChar | 15 | [OACT](OACT.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LogInstanc |
