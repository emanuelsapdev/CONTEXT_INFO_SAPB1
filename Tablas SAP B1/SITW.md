# SITW - Items - Warehouse

- **Tabla:** SITW
- **Descripción:** Items - Warehouse
- **Cantidad de campos:** 75
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SITW.html

## Campos (75)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 2 | `WhsCode` | Warehouse Code | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 3 | `OnHand` | In Stock | Num | 19.6 | - |  |  |
| 4 | `IsCommited` | Defined | Num | 19.6 | - |  |  |
| 5 | `OnOrder` | Ordered | Num | 19.6 | - |  |  |
| 6 | `Consig` | Consignment Goods Whse | Num | 19.6 | - |  |  |
| 7 | `Counted` | Counted Quantity | Num | 19.6 | - |  |  |
| 8 | `WasCounted` | Counted Yes/No | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 9 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 10 | `MinStock` | Minimum Inventory | Num | 19.6 | - |  |  |
| 11 | `MaxStock` | Maximum Inventory | Num | 19.6 | - |  |  |
| 12 | `MinOrder` | Min. Order | Num | 19.6 | - |  |  |
| 13 | `AvgPrice` | Average Price | Num | 19.6 | - |  |  |
| 14 | `Locked` | Locked | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 15 | `BalInvntAc` | Inventory Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 16 | `SaleCostAc` | Cost of Goods Sold Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 17 | `TransferAc` | Transfer Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 18 | `RevenuesAc` | Revenue Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 19 | `VarianceAc` | Variance Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 20 | `DecreasAc` | Inventory Offset - Decrease Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 21 | `IncreasAc` | Inventory Offset - Increase Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 22 | `ReturnAc` | Sales Returns Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 23 | `ExpensesAc` | Expense Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 24 | `EURevenuAc` | Revenue Account - EU | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 25 | `EUExpensAc` | Expense Account - EU | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 26 | `FrRevenuAc` | Revenue Account - Foreign | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 27 | `FrExpensAc` | Expense Account - Foreign | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 28 | `ExmptIncom` | Exempt Revenue Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 29 | `PriceDifAc` | Price Differences Account | nVarChar | 15 | - |  |  |
| 30 | `ExchangeAc` | Exchange Rate Differences Account | nVarChar | 15 | - |  |  |
| 31 | `BalanceAcc` | Goods Clearing Account | nVarChar | 15 | - |  |  |
| 32 | `PurchaseAc` | Purchase Account | nVarChar | 15 | - |  |  |
| 33 | `PAReturnAc` | Purchase Return Account | nVarChar | 15 | - |  |  |
| 34 | `PurchOfsAc` | Purchase Offset Account | nVarChar | 15 | - |  |  |
| 35 | `ShpdGdsAct` | Shipped Goods Account | nVarChar | 15 | - |  |  |
| 36 | `VatRevAct` | VAT in Revenue Account | nVarChar | 15 | - |  |  |
| 37 | `StockValue` | Inventory Value | Num | 19.6 | - |  |  |
| 38 | `DecresGlAc` | G/L Decrease Account | nVarChar | 15 | - |  |  |
| 39 | `IncresGlAc` | G/L Increase Account | nVarChar | 15 | - |  |  |
| 40 | `StokRvlAct` | Stock Inflation Adjust Account | nVarChar | 15 | - |  |  |
| 41 | `StkOffsAct` | Stock Inflation Offset Account | nVarChar | 15 | - |  |  |
| 42 | `WipAcct` | WIP Inventory Account | nVarChar | 15 | - |  |  |
| 43 | `WipVarAcct` | WIP Inventory Variance Account | nVarChar | 15 | - |  |  |
| 44 | `CostRvlAct` | Cost Inflation Account | nVarChar | 15 | - |  |  |
| 45 | `CstOffsAct` | Cost Inflation Offset Account | nVarChar | 15 | - |  |  |
| 46 | `ExpClrAct` | Expense Clearing Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 47 | `ExpOfstAct` | Expense Offset Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 48 | `Object` | Object Type - History | nVarChar | 20 | - | 31 |  |
| 49 | `logInstanc` | Log Instance - History | Int | 11 | - |  |  |
| 50 | `createDate` | Creation Date - History | Date | 8 | - |  |  |
| 51 | `userSign2` | Updating User - History | Int | 6 | [OUSR](OUSR.md) |  |  |
| 52 | `updateDate` | Date of Update - History | Date | 8 | - |  |  |
| 53 | `ARCMAct` | Sales Credit Account | nVarChar | 15 | - |  |  |
| 54 | `ARCMFrnAct` | Sales Credit Account - Foreign | nVarChar | 15 | - |  |  |
| 55 | `ARCMEUAct` | Sales Credit Account - EU | nVarChar | 15 | - |  |  |
| 56 | `ARCMExpAct` | Tax Exempt Credit Account | nVarChar | 15 | - |  |  |
| 57 | `APCMAct` | Purchase Credit Account | nVarChar | 15 | - |  |  |
| 58 | `APCMFrnAct` | Purchase Credit Account - Foreign | nVarChar | 15 | - |  |  |
| 59 | `APCMEUAct` | Purchase Credit Account - EU | nVarChar | 15 | - |  |  |
| 60 | `RevRetAct` | Revenue Returns Account | nVarChar | 15 | - |  |  |
| 61 | `NegStckAct` | Negative Inventory Adj. Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 62 | `StkInTnAct` | Stock In Transit Account | nVarChar | 15 | - |  |  |
| 63 | `PurBalAct` | Purchase Balance Account | nVarChar | 15 | - |  |  |
| 64 | `WhICenAct` | Incoming CENVAT Account (WH) | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 65 | `WhOCenAct` | Outgoing CENVAT Account (WH) | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 66 | `WipOffset` | WIP Offset P&L Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 67 | `StockOffst` | Inventory Offset P&L Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 68 | `DftBinAbs` | Default Bin Internal Number | Int | 11 | [OBIN](OBIN.md) |  |  |
| 69 | `DftBinEnfd` | Default Bin Enforced [Y/N] | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 70 | `Freezed` | Item Frozen in Warehouse | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 71 | `FreezeDoc` | INC Document Frozen By | Int | 11 | [OINC](OINC.md) |  |  |
| 72 | `FreeChrgSA` | Free of Charge Sales Account | nVarChar | 15 | - |  |  |
| 73 | `FreeChrgPU` | Free of Charge Purchase Account | nVarChar | 15 | - |  |  |
| 74 | `IndEscala` | Indicator for Relevant Scale | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 75 | `CNJPMan` | CNPJ of Manufacturer | nVarChar | 14 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ItemCode, WhsCode |
| WHS | No | WhsCode |
