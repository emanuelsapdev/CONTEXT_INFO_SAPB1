# OGAR - G/L Account Advanced Rules

- **Tabla:** OGAR
- **Descripción:** G/L Account Advanced Rules
- **Cantidad de campos:** 89
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OGAR.html

## Campos (89)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
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
| 17 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 18 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 19 | `ItmsGrpCod` | Item Group | Int | 6 | [OITB](OITB.md) |  |  |
| 20 | `WhsCode` | Warehouse Code | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 21 | `BPGrpCod` | BP Group | Int | 6 | [OCRG](OCRG.md) |  |  |
| 22 | `LicTradNum` | Federal Tax ID | nVarChar | 32 | - | !^\| | `!^\|` = All<br>`!^\|E` = Empty<br>`!^\|F` = Filled<br>`Enter Tax ID` = Enter Tax ID |
| 23 | `ShipCountr` | Ship-to Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 24 | `ShipState` | Ship-To State | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 25 | `Comments` | Remarks | nVarChar | 254 | - |  |  |
| 26 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 27 | `RuleCode` | Advanced Rule Code | nVarChar | 20 | - |  |  |
| 28 | `GLMethod` | Get G/L Account By | VarChar | 1 | - | A | `A` = General<br>`W` = Warehouse<br>`C` = Item Group |
| 29 | `Transfered` | Year Transfer [Y/N] | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 30 | `FromDate` | From Date | Date | 8 | - |  |  |
| 31 | `ToDate` | To Date | Date | 8 | - |  |  |
| 32 | `DfltExpn` | Expense Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 33 | `DfltIncom` | Revenue Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 34 | `ExmptIncom` | Tax Exempt Revenue Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 35 | `StockAct` | Inventory Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 36 | `COGM_Act` | Cost of Goods Sold Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 37 | `AlocCstAct` | Allocation Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 38 | `VariancAct` | Variance Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 39 | `PricDifAct` | Price Difference Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 40 | `NegStckAct` | Negative Inventory Adj. Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 41 | `DfltLoss` | Inventory Offset - Decr. Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 42 | `DfltProfit` | Inventory Offset - Incr. Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 43 | `RturnngAct` | Sales Returns Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 44 | `ECIncome` | Revenue Account - EU | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 45 | `ECExepnses` | Expense Account - EU | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 46 | `ForgnIncm` | Revenue Account - Foreign | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 47 | `ForgnExpn` | Expense Account - Foreign | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 48 | `PurchseAct` | Purchase Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 49 | `PaReturnAc` | Purchase Return Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 50 | `PaOffsetAc` | Purchase Offset Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 51 | `ExDiffAct` | Exchange Rate Differences Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 52 | `BalanceAct` | Goods Clearing Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 53 | `DecresGlAc` | G/L Decrease Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 54 | `IncresGlAc` | G/L Increase Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 55 | `WipAcct` | WIP Inventory Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 56 | `WipVarAcct` | WIP Inventory Variance Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 57 | `WipOffset` | WIP Offset P&L Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 58 | `StockOffst` | Inventory Offset P&L Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 59 | `StockRvAct` | Inventory Revaluation Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 60 | `StkRvOfAct` | Inventory Reval. Offset Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 61 | `CostRevAct` | COGS Revaluation Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 62 | `CostOffAct` | COGS Revaluation Offset Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 63 | `ExpClrAct` | Expense Clearing Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 64 | `ExpOfstAct` | Expense Offset Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 65 | `StkInTnAct` | Stock In Transit Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 66 | `ShpdGdsAct` | Shipped Goods Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 67 | `VatRevAct` | VAT in Revenue Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 68 | `ARCMAct` | Sales Credit Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 69 | `APCMAct` | Purchase Credit Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 70 | `ARCMExpAct` | Tax Exempt Credit Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 71 | `ARCMFrnAct` | Sales Credit Account - Foreign | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 72 | `APCMFrnAct` | Purchase Credit Acct - Foreign | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 73 | `ARCMEUAct` | Sales Credit Account - EU | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 74 | `APCMEUAct` | Purchase Credit Account - EU | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 75 | `PurBalAct` | Purchase Balance Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 76 | `WhICenAct` | Incoming CENVAT Account (WH) | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 77 | `WhOCenAct` | Outgoing CENVAT Account (WH) | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 78 | `Active` | Is Rule Active | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 79 | `CmpPrivate` | Company/Private/Government | VarChar | 1 | - | A | `A` = All<br>`C` = Company<br>`I` = Private<br>`G` = Government |
| 80 | `VatGroup` | Tax Definition | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 81 | `CardCode` | Customer/Vendor Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 82 | `Usage` | Usage Code for Document | Int | 11 | [OUSG](OUSG.md) |  |  |
| 83 | `FreeChrgSA` | Free of Charge Sales Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 84 | `FreeChrgPU` | Free of Charge Purchase Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 85 | `UDF1` | User Defined Field 1 | nVarChar | 254 | - |  |  |
| 86 | `UDF2` | User Defined Field 2 | nVarChar | 254 | - |  |  |
| 87 | `UDF3` | User Defined Field 3 | nVarChar | 254 | - |  |  |
| 88 | `UDF4` | User Defined Field 4 | nVarChar | 254 | - |  |  |
| 89 | `UDF5` | User Defined Field 5 | nVarChar | 254 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
