# AITB - Item Groups - History

- **Tabla:** AITB
- **Descripción:** Item Groups - History
- **Cantidad de campos:** 82
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AITB.html

## Campos (82)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ItmsGrpCod` | Number | Int | 6 | - |  |  |
| 2 | `ItmsGrpNam` | Group Name | nVarChar | 100 | - |  |  |
| 3 | `Locked` | Locked | VarChar | 1 | - | N | `N` = Changeable<br>`Y` = Locked |
| 4 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 5 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 6 | `BalInvntAc` | Inventory Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 7 | `SaleCostAc` | Cost Of Goods Sold | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 8 | `TransferAc` | Allocation Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 9 | `RevenuesAc` | Revenue Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 10 | `VarianceAc` | Variance Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 11 | `DecreasAc` | Inventory Offset - Decrease | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 12 | `IncreasAc` | Inventory Offset - Increase | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 13 | `ReturnAc` | Sales Returns | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 14 | `ExpensesAc` | Expense Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 15 | `EURevenuAc` | Sales Revenue - EU | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 16 | `EUExpensAc` | EU Expense Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 17 | `FrRevenuAc` | Sales Revenue - Foreign | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 18 | `FrExpensAc` | Foreign Expense Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 19 | `ExmptIncom` | Exempt Revenue Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 20 | `CycleCode` | Cycle Code | Int | 6 | [OCYC](OCYC.md) |  |  |
| 21 | `Alert` | Alert | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 22 | `PriceDifAc` | Price Difference Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 23 | `ExchangeAc` | Exchange Rate Differences Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 24 | `BalanceAcc` | Goods Clearing Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 25 | `PurchaseAc` | Purchase Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 26 | `PAReturnAc` | PA Return Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 27 | `PurchOfsAc` | Purchase Offset Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 28 | `ShpdGdsAct` | Shipped Goods Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 29 | `VatRevAct` | VAT in Revenue Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 30 | `DecresGlAc` | G/L Decrease Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 31 | `IncresGlAc` | G/L Increase Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 32 | `InvntSys` | Inventory System | VarChar | 1 | - |  | `A` = Moving Average<br>`S` = Standard<br>`F` = FIFO |
| 33 | `PlaningSys` | Planning Method | VarChar | 1 | - | N | `M` = MRP<br>`N` = None |
| 34 | `PrcrmntMtd` | Procurement Method | VarChar | 1 | - | B | `B` = Buy<br>`M` = Make |
| 35 | `OrdrIntrvl` | Order Interval | Int | 6 | [OCYC](OCYC.md) |  |  |
| 36 | `OrdrMulti` | Order Multiple | Num | 19.6 | - |  |  |
| 37 | `MinOrdrQty` | Minimum Order Quantity | Num | 19.6 | - |  |  |
| 38 | `LeadTime` | Lead Time | Int | 11 | - |  |  |
| 39 | `StokRvlAct` | Inventory Revaluation Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 40 | `StkOffsAct` | Inventory Revaluation Offset Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 41 | `WipAcct` | WIP Material Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 42 | `WipVarAcct` | WIP Material Variance Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 43 | `CostRvlAct` | Cost of Sale Revaluation Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 44 | `CstOffsAct` | Cost of Sales Reval. Offs. Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 45 | `ExpClrAct` | Expenses Clearing Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 46 | `ExpOfstAct` | Expense Offset Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 47 | `Object` | Object Type - History | nVarChar | 20 | - | 52 |  |
| 48 | `logInstanc` | Log Instance - History | Int | 11 | - |  |  |
| 49 | `createDate` | Creation Date - History | Date | 8 | - |  |  |
| 50 | `userSign2` | Updating User - History | Int | 6 | [OUSR](OUSR.md) |  |  |
| 51 | `updateDate` | Update Date - History | Date | 8 | - |  |  |
| 52 | `ARCMAct` | Sales Credit Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 53 | `ARCMFrnAct` | Sales Credit Foreign Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 54 | `ARCMEUAct` | Sales Credit EU Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 55 | `ARCMExpAct` | Exempted Credits | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 56 | `APCMAct` | Purchase Credit Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 57 | `APCMFrnAct` | Foreign Purchase Credit Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 58 | `APCMEUAct` | EU Purchase Credit Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 59 | `RevRetAct` | Revenue Returns Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 60 | `ItemClass` | Service or Material | VarChar | 1 | - | 2 | `1` = Service<br>`2` = Material |
| 61 | `OSvcCode` | Outgoing Service Code | Int | 11 | [OSCD](OSCD.md) | -1 |  |
| 62 | `ISvcCode` | Incoming Service Code | Int | 11 | [OSCD](OSCD.md) | -1 |  |
| 63 | `ServiceGrp` | Service Group | Int | 11 | [OSGP](OSGP.md) | -1 |  |
| 64 | `NCMCode` | NCM Code | Int | 11 | [ONCM](ONCM.md) | -1 |  |
| 65 | `MatType` | Material Type | nVarChar | 3 | [OMTP](OMTP.md) | 1 |  |
| 66 | `MatGrp` | Material Group | Int | 11 | [OMGP](OMGP.md) | -1 |  |
| 67 | `ProductSrc` | Product Source | nVarChar | 2 | [OPSC](OPSC.md) | 0 |  |
| 68 | `NegStckAct` | Negative Inventory Adjustment | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 69 | `StkInTnAct` | Stock In Transit Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 70 | `PurBalAct` | Purchase Balance Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 71 | `WhICenAct` | Incoming CENVAT Account (WH) | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 72 | `WhOCenAct` | Outgoing CENVAT Account (WH) | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 73 | `WipOffset` | WIP Offset P&L Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 74 | `StockOffst` | Inventory Offset P&L Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 75 | `UgpEntry` | Default UoM Group Entry | Int | 11 | [OUGP](OUGP.md) |  |  |
| 76 | `IUoMEntry` | Default Inventory UoM | Int | 11 | [OUOM](OUOM.md) |  |  |
| 77 | `ToleranDay` | Tolerance Days | Int | 11 | - |  |  |
| 78 | `RuleCode` | Checking Rule Code | nVarChar | 2 | [ODCR](ODCR.md) |  |  |
| 79 | `CompoWH` | Component Warehouse | VarChar | 1 | - | B | `B` = From Bill of Materials Line<br>`P` = From Parent Item Document Line |
| 80 | `FreeChrgSA` | Free of Charge Sales Account | nVarChar | 15 | - |  |  |
| 81 | `FreeChrgPU` | Free of Charge Purchase Account | nVarChar | 15 | - |  |  |
| 82 | `RawMtrl` | Raw Material | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ItmsGrpCod, logInstanc |
| GROUP_NAME | No | ItmsGrpNam, logInstanc |
