# UIVL - Whse Journal

- **Tabla:** UIVL
- **Descripción:** Whse Journal
- **Cantidad de campos:** 78
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UIVL.html

## Campos (78)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TransType` | Transaction Type | Int | 11 | - | -1 | `15` = Delivery<br>`16` = Returns<br>`13` = A/R Invoice<br>`14` = A/R Credit Memo<br>`132` = Correction Invoice<br>`20` = Goods Receipt<br>`21` = Goods Return<br>`18` = A/P Invoice<br>`19` = A/P Credit Memo<br>`-2` = Opening Balance<br>`58` = Inventory Update<br>`59` = Goods Receipt<br>`60` = Goods Issue<br>`67` = Inventory Transfer<br>`68` = Work Instructions<br>`-1` = All Transactions<br>`162` = Inventory Revaluation<br>`69` = Landed Costs |
| 2 | `CreatedBy` | Document No. Created | Int | 11 | - |  |  |
| 3 | `BASE_REF` | Base Reference | nVarChar | 11 | - |  |  |
| 4 | `DocLineNum` | Row Number in Document | Int | 11 | - |  |  |
| 5 | `DocDate` | Posting Date | Date | 8 | - |  |  |
| 6 | `CreateTime` | Generation Time | Int | 6 | - |  |  |
| 7 | `ItemCode` | Item No. | nVarChar | 50 | [UITM](UITM.md) |  |  |
| 8 | `InQty` | Receipt Quantity | Num | 19.6 | - |  |  |
| 9 | `OutQty` | Issue Quantity | Num | 19.6 | - |  |  |
| 10 | `Price` | Price | Num | 19.6 | - |  |  |
| 11 | `Currency` | Price Currency | nVarChar | 3 | - |  |  |
| 12 | `Rate` | Currency Price | Num | 19.6 | - |  |  |
| 13 | `TrnsfrAct` | Transfer Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 14 | `PriceDifAc` | Price Difference Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 15 | `VarianceAc` | Variance Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 16 | `ReturnAct` | Returning Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 17 | `ExcRateAct` | Exchange Rate Differences Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 18 | `ClearAct` | Goods Clearing Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 19 | `CostAct` | COGS Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 20 | `WipAct` | WIP Inventory Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 21 | `OpenStock` | Open Sum Inventory Value | Num | 19.6 | - |  |  |
| 22 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 23 | `PriceDiff` | Price Difference Value | Num | 19.6 | - |  |  |
| 24 | `TransSeq` | Transaction Sequence No. | Int | 11 | - | 0 |  |
| 25 | `InvntAct` | Inventory Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 26 | `SubLineNum` | Subrow Number | Int | 11 | - | -1 |  |
| 27 | `AppObjLine` | Applied Object Row | Int | 11 | - | -1 |  |
| 28 | `Expenses` | Inventory Expenses | Num | 19.6 | - |  |  |
| 29 | `OpenExp` | Open Expenses Value | Num | 19.6 | - |  |  |
| 30 | `Allocation` | Allocation Amount | Num | 19.6 | - |  |  |
| 31 | `OpenAlloc` | Open Allocation Value | Num | 19.6 | - |  |  |
| 32 | `ExpAlloc` | Expenses Allocation Value | Num | 19.6 | - |  |  |
| 33 | `OExpAlloc` | Open Expenses Allocation Value | Num | 19.6 | - |  |  |
| 34 | `OpenPDiff` | Open Price Diff. Value | Num | 19.6 | - |  |  |
| 35 | `ExchDiff` | Exchange Rate Difference Value | Num | 19.6 | - |  |  |
| 36 | `OpenEDiff` | Open Exchange Rate Diff. Value | Num | 19.6 | - |  |  |
| 37 | `NegInvAdjs` | Negative Inventory Adjustment Value | Num | 19.6 | - |  |  |
| 38 | `OpenNegInv` | Open Negative Adjustment | Num | 19.6 | - |  |  |
| 39 | `NegStckAct` | Neg. Inventory Adjustment Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 40 | `BTransVal` | Base Transaction Value | Num | 19.6 | - |  |  |
| 41 | `VarVal` | Variance Value | Num | 19.6 | - |  |  |
| 42 | `BExpVal` | Base Freight Value | Num | 19.6 | - |  |  |
| 43 | `CogsVal` | COGS Value | Num | 19.6 | - |  |  |
| 44 | `BNegAVal` | Base Negative Adjustment Amt | Num | 19.6 | - |  |  |
| 45 | `IOffIncAcc` | Inventory Offset Increase Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 46 | `IOffIncVal` | Inv. Offset Increase Value | Num | 19.6 | - |  |  |
| 47 | `DOffDecAcc` | Inventory Offset Decrease Acct | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 48 | `DOffDecVal` | Inv. Offset Decrease Value | Num | 19.6 | - |  |  |
| 49 | `DecAcc` | G/L Decrease Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 50 | `DecVal` | G/L Decrease Value | Num | 19.6 | - |  |  |
| 51 | `WipVal` | WIP Inventory Value | Num | 19.6 | - |  |  |
| 52 | `WipVarAcc` | WIP Variance Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 53 | `WipVarVal` | WIP Variance Value | Num | 19.6 | - |  |  |
| 54 | `IncAct` | G/L Increase Account | nVarChar | 15 | - |  |  |
| 55 | `IncVal` | G/L Increase Value | Num | 19.6 | - |  |  |
| 56 | `ExpCAcc` | Expense Clearing Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 57 | `CostMethod` | Costing Method | VarChar | 1 | - | N | `A` = Moving Average<br>`S` = Standard<br>`F` = FIFO<br>`B` = Serial/Batch<br>`N` = None |
| 58 | `MessageID` | Message ID | Int | 11 | [UILM](UILM.md) |  |  |
| 59 | `LocType` | Location Type | Int | 11 | - |  |  |
| 60 | `LocCode` | Warehouse Code | nVarChar | 8 | - |  |  |
| 61 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 62 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Upgrade<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Auto Summary<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`Y` = Year Transfer |
| 63 | `PostStatus` | Posting Status | VarChar | 1 | - | N | `N` = None<br>`P` = Partial<br>`C` = Complete |
| 64 | `SumStock` | Sum Inventory Value | Num | 19.6 | - |  |  |
| 65 | `OpenCogs` | Open COGS Value | Num | 19.6 | - |  |  |
| 66 | `OpenQty` | Open Quantity | Num | 19.6 | - |  |  |
| 67 | `TreeID` | Tree ID | Int | 11 | - | -1 |  |
| 68 | `ParentID` | Parent ID | Int | 11 | - | -1 |  |
| 69 | `PAOffAcc` | Purchase Offset Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 70 | `PAOffVal` | Purchase Offset Value | Num | 19.6 | - |  |  |
| 71 | `OpenPAOff` | Open Purchase Offset Value | Num | 19.6 | - |  |  |
| 72 | `PAAcc` | Purchase Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 73 | `PAVal` | Purchase Account Value | Num | 19.6 | - |  |  |
| 74 | `OpenPA` | Open Purchase Value | Num | 19.6 | - |  |  |
| 75 | `LinkArc` | Linked To Archived Doc | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 76 | `VersionNum` | Version Number | nVarChar | 13 | - |  |  |
| 77 | `BSubLineNo` | Base Subrow Number | Int | 11 | - | -1 |  |
| 78 | `WipDebCred` | WIP Account: Debit/Credit Side | VarChar | 1 | - |  |  |

## Claves e índices (7)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TransSeq |
| ITEM | No | ItemCode |
| CURRENCY | No | Currency |
| DOCDATE | No | DocDate |
| DOCENTRY | No | CreatedBy, TransType, DocLineNum |
| MESSAGEID | No | MessageID |
| TREEID | No | TreeID |
