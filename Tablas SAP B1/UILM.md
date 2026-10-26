# UILM - IVI Inventory Log Message

- **Tabla:** UILM
- **Descripción:** IVI Inventory Log Message
- **Cantidad de campos:** 89
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UILM.html

## Campos (89)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `MessageID` | Message ID | Int | 11 | - |  |  |
| 2 | `DocEntry` | Doc Number | Int | 11 | - |  |  |
| 3 | `TransType` | Transaction Type | Int | 11 | - | -1 |  |
| 4 | `DocLineNum` | Doc Row Number | Int | 11 | - |  |  |
| 5 | `Quantity` | Quantity in Doc | Num | 19.6 | - |  |  |
| 6 | `EffectQty` | Stock Effective Qty | Num | 19.6 | - |  |  |
| 7 | `LocType` | Location Type | Int | 6 | - |  |  |
| 8 | `LocCode` | Location Code | nVarChar | 8 | - |  |  |
| 9 | `TotalLC` | Inventory Total LC | Num | 19.6 | - |  |  |
| 10 | `TotalFC` | Inventory Total FC | Num | 19.6 | - |  |  |
| 11 | `TotalSC` | Inventory Total SC | Num | 19.6 | - |  |  |
| 12 | `BaseAbsEnt` | Internal ID of Base Document | Int | 11 | - |  |  |
| 13 | `BaseType` | Base Transaction Type | Int | 11 | - | -1 | `-1`<br>`0`<br>`13` = A/R Invoice<br>`15` = Delivery<br>`16` = Returns<br>`17` = Sales Order<br>`18` = A/P Invoice<br>`20` = Goods Receipt PO<br>`21` = Goods Return<br>`22` = Purchase Order<br>`23` = Sales Quotation<br>`59` = Goods Receipt<br>`67` = Inventory Transfer<br>`69` = Landed Costs<br>`163` = A/P Correction Invoice<br>`164` = A/P Correction Invoice Reversal<br>`165` = A/R Correction Invoice<br>`166` = A/R Correction Invoice Reversal<br>`202` = Production Order<br>`203` = A/R Down Payment<br>`204` = A/P Down Payment |
| 14 | `BaseCurr` | Base Currency | nVarChar | 3 | - |  |  |
| 15 | `Currency` | Doc Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 16 | `AccumType` | Accumulator Type | Int | 11 | - | 0 | `0` = ACCUM_EMPTY<br>`1` = ACCUM_ON_HAND<br>`2` = ACCUM_COMMITTED<br>`3` = ACCUM_ON_ORDER<br>`4` = ACCUM_CONSIGNATION<br>`5` = ACCUM_COUNTED |
| 17 | `ActionType` | Action Type | Int | 11 | - | 5 | `0` = TRANSACTION_UNKNOWN<br>`1` = TRANSACTION_IN<br>`2` = TRANSACTION_OUT<br>`3` = TRANSACTION_SET<br>`4` = TRANSACTION_COMPLETE<br>`5` = EMPTY_TRANSACTION<br>`6` = TRANSACTION_REVALUATION<br>`7` = TRANSACTION_REVALUATION_INCREASE<br>`8` = TRANSACTION_REVALUATION_DECREASE<br>`9` = TRANSACTION_CLOSE_IN<br>`10` = TRANSACTION_CLOSE_OUT<br>`11` = TRANSACTION_NEGATIVE_REVALUATION<br>`12` = TRANSACTION_NULLIFY<br>`13` = TRANSACTION_RESERVE_CI_IN<br>`14` = TRANSACTION_RESERVE_CI_OUT<br>`15` = TRANSACTION_RESERVE_CI_REVAL_INC<br>`16` = TRANSACTION_RESERVE_CI_REVAL_DEC<br>`17` = TRANSACTION_REVAL_PRICE_CHANGE_INCREASE<br>`18` = TRANSACTION_REVAL_PRICE_CHANGE_DECREASE |
| 18 | `ExpensesLC` | Expenses (LC) | Num | 19.6 | - |  |  |
| 19 | `ExpensesFC` | Expenses (FC) | Num | 19.6 | - |  |  |
| 20 | `ExpensesSC` | Expenses (SC) | Num | 19.6 | - |  |  |
| 21 | `DocDueDate` | Doc. Due Date | Date | 8 | - |  |  |
| 22 | `ItemCode` | Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 23 | `BPCardCode` | Business Partner Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 24 | `DocDate` | Doc Date | Date | 8 | - |  |  |
| 25 | `DocRate` | Doc. Rate | Num | 19.6 | - |  |  |
| 26 | `Comment` | Comment | nVarChar | 254 | - |  |  |
| 27 | `JrnlMemo` | Journal Remarks | nVarChar | 50 | - |  |  |
| 28 | `Ref1` | Reference 1 | nVarChar | 11 | - |  |  |
| 29 | `Ref2` | Reference 2 | nVarChar | 100 | - |  |  |
| 30 | `BaseLine` | Base Row Number | Int | 11 | - | -1 |  |
| 31 | `SnBType` | Serials and Batches Type | Int | 11 | - | -1 | `0` = Batch Numbers Management<br>`1` = Serial Number Management |
| 32 | `CreateTime` | Generation Time | Int | 6 | - |  |  |
| 33 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 34 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 35 | `OcrCode` | Distribution Rule | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 36 | `OcrCode2` | Distribution Rule2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 37 | `OcrCode3` | Distribution Rule3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 38 | `OcrCode4` | Distribution Rule4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 39 | `OcrCode5` | Distribution Rule5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 40 | `DocPrice` | Doc Price | Num | 19.6 | - |  |  |
| 41 | `CardName` | BP Name | nVarChar | 200 | - |  |  |
| 42 | `Dscription` | Item Description | nVarChar | 200 | - |  |  |
| 43 | `TreeType` | BOM Type | VarChar | 1 | - | N | `N` = Not a BOM<br>`A` = Assembly<br>`S` = Sales<br>`I` = BOM Component Item<br>`P` = Production<br>`T` = Template |
| 44 | `ApplObj` | Applied Object | Int | 11 | - | -1 |  |
| 45 | `AppObjAbs` | Applied Object Internal ID | Int | 11 | - | -1 |  |
| 46 | `AppObjType` | Applied Object Type | VarChar | 1 | - |  |  |
| 47 | `AppObjLine` | Applied Object Row | Int | 11 | - | -1 |  |
| 48 | `BASE_REF` | Base Reference | nVarChar | 11 | - |  |  |
| 49 | `TransSeqRf` | Transaction Sequence Ref | Int | 11 | - | -1 |  |
| 50 | `LayerIDRef` | Layer ID Reference | Int | 11 | - | -1 |  |
| 51 | `VersionNum` | Version Number | nVarChar | 13 | - |  |  |
| 52 | `PriceRate` | Price Rate | Num | 19.6 | - |  |  |
| 53 | `PriceCurr` | Price Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 54 | `DocTotal` | Document Total | Num | 19.6 | - |  |  |
| 55 | `Price` | Price | Num | 19.6 | - |  |  |
| 56 | `CIShbQty` | Corr. Inv. Doc. Should Be Qty | Num | 19.6 | - |  |  |
| 57 | `SubLineNum` | Sub Line Number | Int | 11 | - | -1 |  |
| 58 | `PrjCode` | Project code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 59 | `SlpCode` | Sales Employee | Int | 11 | [OSLP](OSLP.md) | -1 |  |
| 60 | `TaxDate` | Document Date | Date | 8 | - |  |  |
| 61 | `UseDocPric` | Use Document Price | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 62 | `VendorNum` | Vendor Catalog No. | nVarChar | 50 | - |  |  |
| 63 | `SerialNum` | Serial Number | nVarChar | 17 | - |  |  |
| 64 | `BlockNum` | Block Number | nVarChar | 100 | - |  |  |
| 65 | `ImportLog` | Import Log | nVarChar | 20 | - |  |  |
| 66 | `Location` | Location | Int | 11 | [OLCT](OLCT.md) |  |  |
| 67 | `DocPrcRate` | Document Price Rate | Num | 19.6 | - |  |  |
| 68 | `DocPrcCurr` | Document Price Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 69 | `CgsOcrCod` | COGS Distribution Rule | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 70 | `CgsOcrCod2` | COGS Distribution Rule 2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 71 | `CgsOcrCod3` | COGS Distribution Rule 3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 72 | `CgsOcrCod4` | COGS Distribution Rule 4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 73 | `CgsOcrCod5` | COGS Distribution Rule 5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 74 | `BSubLineNo` | Base Subrow Number | Int | 11 | - | -1 |  |
| 75 | `AppSubLine` | Applied Subrow Number | Int | 11 | - | -1 |  |
| 76 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 77 | `SysRate` | System Rate | Num | 19.6 | - |  |  |
| 78 | `ExFromRpt` | Exclude from Report | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 79 | `Ref3` | Reference 3 | nVarChar | 100 | - |  |  |
| 80 | `EnSetCost` | Enable Set Item Cost in Return | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 81 | `RetCost` | Return Cost in A/R Return | Num | 19.6 | - |  |  |
| 82 | `DocAction` | Document Action Type | Int | 11 | - |  |  |
| 83 | `UseShpdGd` | Use Shipped Goods Account | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 84 | `AddTotalLC` | Additional Total LC | Num | 19.6 | - |  |  |
| 85 | `AddExpLC` | Additional Expenses LC | Num | 19.6 | - |  |  |
| 86 | `IsNegLnQty` | Negative Line Quantity | VarChar | 1 | - | N |  |
| 87 | `StgSeqNum` | Stage Sequence Number | Int | 11 | - |  |  |
| 88 | `StgEntry` | Stage Entry | Int | 11 | - |  |  |
| 89 | `StgDesc` | Stage Description | nVarChar | 100 | - |  |  |

## Claves e índices (6)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | MessageID |
| CARD | No | BPCardCode |
| DocLine | No | TransType, DocEntry, DocLineNum, SubLineNum |
| APPOBJ | No | ApplObj, AppObjAbs, AppObjType, AppObjLine |
| BASEOBJ | No | BaseType, BaseAbsEnt, BaseLine, BSubLineNo |
| EntryType | No | DocEntry, TransType, MessageID |
