# AWHS - Warehouses - History

- **Tabla:** AWHS
- **Descripción:** Warehouses - History
- **Cantidad de campos:** 103
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AWHS.html

## Campos (103)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WhsCode` | Warehouse Code | nVarChar | 8 | - |  |  |
| 2 | `WhsName` | Warehouse Name | nVarChar | 100 | - |  |  |
| 3 | `IntrnalKey` | Internal Key | Int | 11 | - |  |  |
| 4 | `Grp_Code` | Group Code | nVarChar | 4 | - |  |  |
| 5 | `BalInvntAc` | Inventory Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 6 | `SaleCostAc` | Cost of Goods Sold Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 7 | `TransferAc` | Allocation Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 8 | `Locked` | Locked | VarChar | 1 | - | N | `N` = Changeable<br>`Y` = Locked |
| 9 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 10 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 11 | `RevenuesAc` | Revenue Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 12 | `VarianceAc` | Variance Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 13 | `DecreasAc` | Inventory Offset - Decrease Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 14 | `IncreasAc` | Inventory Offset - Increase Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 15 | `ReturnAc` | Sales Returns Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 16 | `ExpensesAc` | Expense Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 17 | `EURevenuAc` | Revenue Account - EU | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 18 | `EUExpensAc` | Expense Account - EU | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 19 | `FrRevenuAc` | Revenue Account - Foreign | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 20 | `FrExpensAc` | Expense Account - Foreign | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 21 | `VatGroup` | Tax Group | nVarChar | 8 | [OSTC](OSTC.md) |  |  |
| 22 | `Street` | Street | nVarChar | 100 | - |  |  |
| 23 | `Block` | Block | nVarChar | 100 | - |  |  |
| 24 | `ZipCode` | Zip Code | nVarChar | 20 | - |  |  |
| 25 | `City` | City | nVarChar | 100 | - |  |  |
| 26 | `County` | County | nVarChar | 100 | [OCNT](OCNT.md) |  |  |
| 27 | `Country` | Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 28 | `State` | Status | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 29 | `Location` | Location | Int | 11 | [OLCT](OLCT.md) |  |  |
| 30 | `DropShip` | Drop-Ship | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 31 | `ExmptIncom` | Exempt Revenue Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 32 | `UseTax` | Allow Use Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 33 | `PriceDifAc` | Price Difference Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 34 | `ExchangeAc` | Exchange Rate Differences Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 35 | `BalanceAcc` | Goods Clearing Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 36 | `PurchaseAc` | Purchase Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 37 | `PAReturnAc` | Purchase Return Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 38 | `PurchOfsAc` | Purchase Offset Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 39 | `FedTaxID` | Federal Tax ID | nVarChar | 32 | - |  |  |
| 40 | `Building` | Building/Floor/Room | Text | 16 | - |  |  |
| 41 | `ShpdGdsAct` | Shipped Goods Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 42 | `VatRevAct` | VAT in Revenue Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 43 | `DecresGlAc` | G/L Decrease Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 44 | `IncresGlAc` | G/L Increase Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 45 | `Nettable` | Nettable | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 46 | `StokRvlAct` | Inventory Revaluation Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 47 | `StkOffsAct` | Inventory Revaluation Offset Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 48 | `WipAcct` | WIP Inventory Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 49 | `WipVarAcct` | WIP Inventory Variance Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 50 | `CostRvlAct` | COGS Revaluation Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 51 | `CstOffsAct` | COGS Revaluation Offset Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 52 | `ExpClrAct` | Expense Clearing Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 53 | `ExpOfstAct` | Expense Offset Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 54 | `objType` | Object Type - History | nVarChar | 20 | - | 64 |  |
| 55 | `logInstanc` | Log Instance - History | Int | 11 | - |  |  |
| 56 | `createDate` | Creation Date - History | Date | 8 | - |  |  |
| 57 | `userSign2` | Updating User - History | Int | 6 | [OUSR](OUSR.md) |  |  |
| 58 | `updateDate` | Date of Update - History | Date | 8 | - |  |  |
| 59 | `ARCMAct` | Sales Credit Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 60 | `ARCMFrnAct` | Sales Credit Foreign Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 61 | `ARCMEUAct` | Sales Credit EU Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 62 | `ARCMExpAct` | Exempted Credits | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 63 | `APCMAct` | Purchase Credit Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 64 | `APCMFrnAct` | Foreign Purchase Credit Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 65 | `APCMEUAct` | EU Purchase Credit Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 66 | `RevRetAct` | Revenue Returns Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 67 | `BPLid` | Business Place ID | Int | 11 | [OBPL](OBPL.md) |  |  |
| 68 | `OwnerCode` | Owner Code | VarChar | 1 | - | 1 | `1` = Company Item Property<br>`2` = Third-Party Warehouse<br>`3` = Third-Party Warehouse |
| 69 | `NegStckAct` | Negative Stock Adjustment Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 70 | `StkInTnAct` | Stock In Transit Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 71 | `AddrType` | Address Type | nVarChar | 100 | - |  |  |
| 72 | `StreetNo` | Street No. | nVarChar | 100 | - |  |  |
| 73 | `PurBalAct` | Purchase Balance Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 74 | `Excisable` | Excisable [Yes/No] | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 75 | `WhICenAct` | Incoming CENVAT Account (WH) | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 76 | `WhOCenAct` | Outgoing CENVAT Account (WH) | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 77 | `WhShipTo` | Ship-to Name (WH) | nVarChar | 100 | - |  |  |
| 78 | `WipOffset` | WIP Offset P&L Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 79 | `StockOffst` | Inventory Offset P&L Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 80 | `StorKeeper` | Storekeeper | Int | 11 | [OHEM](OHEM.md) |  |  |
| 81 | `Shipper` | Shipper | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 82 | `BinActivat` | Bin Activated [Y/N] | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 83 | `BinSeptor` | Bin Separator | nVarChar | 5 | - | - |  |
| 84 | `DftBinAbs` | Default Bin Internal Number | Int | 11 | [OBIN](OBIN.md) |  |  |
| 85 | `DftBinEnfd` | Default Bin Enforced [Y/N] | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 86 | `AutoIssMtd` | Auto. Issue Method | Int | 6 | - | 0 | `0` = Single Choice<br>`1` = Bin Location Code Order<br>`2` = Alternative Sort Code Order<br>`3` = Descending Quantity<br>`4` = Ascending Quantity<br>`7` = Ascending Quantity - Single Bin Preferred<br>`5` = FIFO<br>`6` = LIFO |
| 87 | `ManageSnB` | Drop-Ship Manage SnB | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 88 | `RecItemsBy` | Receiving Bin Locations Method | Int | 6 | - | 0 | `0` = Bin Location Code Order<br>`1` = Alternative Sort Code Order |
| 89 | `RecBinEnab` | Enable Receiving Bin Locations | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 90 | `GlblLocNum` | Global Location Number | nVarChar | 50 | - |  |  |
| 91 | `RecvEmpBin` | Restrict Receipts to Empty Bin | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 92 | `Inactive` | Inactive | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 93 | `RecvMaxQty` | Recv. up to Max. Qty | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 94 | `AutoRecvMd` | Auto. Receipt Method | Int | 6 | - | 0 | `0` = Default Bin Location<br>`1` = Last Bin Location That Received Item<br>`2` = Item's Current Bin Locations<br>`3` = Item's Current and Historical Bin Locations |
| 95 | `RecvMaxWT` | Recv. up to Max. Weight | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 96 | `RecvUpTo` | Receive up to | nVarChar | 6 | - | 0 | `0` = Maximum Qty<br>`1` = Maximum Weight<br>`2` = Max. Qty and Weight |
| 97 | `FreeChrgSA` | Free of Charge Sales Account | nVarChar | 15 | - |  |  |
| 98 | `FreeChrgPU` | Free of Charge Purchase Account | nVarChar | 15 | - |  |  |
| 99 | `TaxOffice` | Tax Office | nVarChar | 50 | - |  |  |
| 100 | `Address2` | Address Name 2 | nVarChar | 50 | - |  |  |
| 101 | `Address3` | Address Name 3 | nVarChar | 50 | - |  |  |
| 102 | `External` | External | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 103 | `LegalText` | Legal Text | nVarChar | 250 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WhsCode, logInstanc |
