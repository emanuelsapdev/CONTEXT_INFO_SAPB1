# GPA1 - Gross Profit Adjustment - Documents

- **Tabla:** GPA1
- **Descripción:** Gross Profit Adjustment - Documents
- **Cantidad de campos:** 54
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/GPA1.html

## Campos (54)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | [OGPA](OGPA.md) |  |  |
| 2 | `LineId` | Row No. | Int | 11 | - |  |  |
| 3 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 4 | `ItemName` | Item Description | nVarChar | 200 | - |  |  |
| 5 | `DocType` | Document Type | nVarChar | 20 | - |  |  |
| 6 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 7 | `DocAbs` | Document Abs. Entry | Int | 11 | - |  |  |
| 8 | `DocLineNum` | Document Line Number | Int | 11 | - |  |  |
| 9 | `ManagedBy` | Managed By | Int | 11 | - | -1 | `10000044` = Batch Numbers<br>`10000045` = Serial Numbers<br>`-1` |
| 10 | `Selected` | Choose | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 11 | `DistNumber` | Batch Number | nVarChar | 36 | - |  |  |
| 12 | `PostDate` | Posting Date | Date | 8 | - |  |  |
| 13 | `WhsCode` | Warehouse Code | nVarChar | 8 | - |  |  |
| 14 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 15 | `CogsAcct` | COGS Account Code | nVarChar | 15 | - |  |  |
| 16 | `CogsAmnt` | COGS Amount | Num | 19.6 | - |  |  |
| 17 | `SalesAmnt` | Sales Amount | Num | 19.6 | - |  |  |
| 18 | `GrssProfit` | Row Gross Profit | Num | 19.6 | - |  |  |
| 19 | `COGSByCC` | COGS By Current Cost | Num | 19.6 | - |  |  |
| 20 | `GPByCC` | Gross Profit By Current Cost | Num | 19.6 | - |  |  |
| 21 | `DeltaGP` | Delta Gross Profit | Num | 19.6 | - |  |  |
| 22 | `SalesPrice` | Sales Price | Num | 19.6 | - |  |  |
| 23 | `BatchQt` | Batch Quantity | Num | 19.6 | - |  |  |
| 24 | `SnBAbs` | SnB Abs. Entry | Int | 11 | - |  |  |
| 25 | `AccTotal` | Acct Total | Num | 19.6 | - |  |  |
| 26 | `AccQty` | Acct Qty | Num | 19.6 | - |  |  |
| 27 | `ActionType` | Action Type | Int | 11 | - | 5 | `0` = TRANSACTION_UNKNOWN<br>`1` = TRANSACTION_IN<br>`2` = TRANSACTION_OUT<br>`3` = TRANSACTION_SET<br>`4` = TRANSACTION_COMPLETE<br>`5` = EMPTY_TRANSACTION<br>`6` = TRANSACTION_REVALUATION<br>`7` = TRANSACTION_REVALUATION_INCREASE<br>`8` = TRANSACTION_REVALUATION_DECREASE<br>`9` = TRANSACTION_CLOSE_IN<br>`10` = TRANSACTION_CLOSE_OUT<br>`11` = TRANSACTION_NEGATIVE_REVALUATION<br>`12` = TRANSACTION_NULLIFY<br>`13` = TRANSACTION_RESERVE_CI_IN<br>`14` = TRANSACTION_RESERVE_CI_OUT<br>`15` = TRANSACTION_RESERVE_CI_REVAL_INC<br>`16` = TRANSACTION_RESERVE_CI_REVAL_DEC<br>`17` = TRANSACTION_REVAL_PRICE_CHANGE_INCREASE<br>`18` = TRANSACTION_REVAL_PRICE_CHANGE_DECREASE |
| 28 | `SBAccTotal` | SnB Acct Total | Num | 19.6 | - |  |  |
| 29 | `SBAccQty` | SnB Acct Qty | Num | 19.6 | - |  |  |
| 30 | `BaseType` | Base Type | nVarChar | 20 | - |  |  |
| 31 | `Execute` | Execute | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 32 | `SBCogsAmnt` | SnB COGS Amount | Num | 19.6 | - |  |  |
| 33 | `SBSaleAmnt` | SnB Sales Amount | Num | 19.6 | - |  |  |
| 34 | `SBGrssProf` | SnB Gross Profit | Num | 19.6 | - |  |  |
| 35 | `SBGrPrPerc` | SnB Gross Profit Percentage | Num | 19.6 | - |  |  |
| 36 | `GrPrPerc` | Gross Profit Percentage | Num | 19.6 | - |  |  |
| 37 | `GPPercByCC` | Gross Profit Percentage By Current Cost | Num | 19.6 | - |  |  |
| 38 | `DeltaGPLn` | Delta gross profit calculated for the document line | Num | 19.6 | - |  |  |
| 39 | `Applied` | Applied Adjustment | Num | 19.6 | - |  |  |
| 40 | `SBAccTtAdj` | SnB Acct Total Adjustment | Num | 19.6 | - |  |  |
| 41 | `IsMixed` | Is Mixed Based Document | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 42 | `CogsAmByCC` | Total COGS Amount By Current Cost | Num | 19.6 | - |  |  |
| 43 | `GrssPrByCC` | Total Gross Profit By Current Cost | Num | 19.6 | - |  |  |
| 44 | `LineType` | Wizard Line Type | VarChar | 1 | - | N | `N` = Normal<br>`C` = Chained<br>`I` = Non Based Correction Invoice |
| 45 | `ChDocType` | Chained Document Type | nVarChar | 20 | - |  |  |
| 46 | `ChDocAbs` | Chained Document Abs. Entry | Int | 11 | - |  |  |
| 47 | `WasQty` | Was Line Quantity | Num | 19.6 | - |  |  |
| 48 | `WasCogs` | Was Line COGS Amount | Num | 19.6 | - |  |  |
| 49 | `WasSales` | Was Line Sales Amount | Num | 19.6 | - |  |  |
| 50 | `WasPrice` | Was Line Sales Price | Num | 19.6 | - |  |  |
| 51 | `WasGrProf` | Was Line Gross Profit | Num | 19.6 | - |  |  |
| 52 | `BaseAbs` | Base Document Abs Entry | Int | 11 | - |  |  |
| 53 | `WasNewCogs` | Was Line New Cogs | Num | 19.6 | - |  |  |
| 54 | `ChDocLine` | Chained Document Line | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineId |
