# OAIM - Archive Inventory Message

- **Tabla:** OAIM
- **Descripción:** Archive Inventory Message
- **Cantidad de campos:** 49
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OAIM.html

## Campos (49)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `MessageID` | Message ID | Int | 11 | - |  |  |
| 2 | `DocEntry` | Document Number | Int | 11 | - |  |  |
| 3 | `TransType` | Transaction Type | Int | 11 | - | -1 |  |
| 4 | `DocLineNum` | Document Row Number | Int | 11 | - |  |  |
| 5 | `Quantity` | Quantity in Document | Num | 19.6 | - |  |  |
| 6 | `EffectQty` | Effective Inventory Quantity | Num | 19.6 | - |  |  |
| 7 | `LocType` | Location Type | Int | 6 | - |  |  |
| 8 | `LocCode` | Location Code | nVarChar | 8 | - |  |  |
| 9 | `TotalLC` | Inventory Total LC | Num | 19.6 | - |  |  |
| 10 | `TotalFC` | Inventory Total FC | Num | 19.6 | - |  |  |
| 11 | `BaseAbsEnt` | Internal No. of Base Doc | Int | 11 | - |  |  |
| 12 | `BaseType` | Base Transaction Type | Int | 11 | - | -1 | `-1`<br>`0`<br>`13` = A/R Invoice<br>`15` = Delivery<br>`16` = Returns<br>`17` = Sales Order<br>`18` = A/P Invoice<br>`20` = Goods Receipt PO<br>`21` = Goods Return<br>`22` = Purchase Order<br>`23` = Sales Quotation<br>`59` = Goods Receipt<br>`67` = Inventory Transfer<br>`69` = Landed Costs<br>`163` = A/P Correction Invoice<br>`164` = A/P Correction Invoice Reversal<br>`165` = A/R Correction Invoice<br>`166` = A/R Correction Invoice Reversal<br>`202` = Production Order<br>`203` = A/R Down Payment<br>`204` = A/P Down Payment |
| 13 | `Currency` | Document Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 14 | `AccumType` | Accumulator Type | Int | 11 | - | 0 | `0` = ACCUM_EMPTY<br>`1` = ACCUM_ON_HAND<br>`2` = ACCUM_COMMITTED<br>`3` = ACCUM_ON_ORDER<br>`4` = ACCUM_CONSIGNATION<br>`5` = ACCUM_COUNTED |
| 15 | `ActionType` | Action Type | Int | 11 | - | 5 | `0` = TRANSACTION_UNKNOWN<br>`1` = TRANSACTION_IN<br>`2` = TRANSACTION_OUT<br>`3` = TRANSACTION_SET<br>`4` = TRANSACTION_COMPLETE<br>`5` = EMPTY_TRANSACTION<br>`6` = TRANSACTION_REVALUATION<br>`7` = TRANSACTION_REVALUATION_INCREASE<br>`8` = TRANSACTION_REVALUATION_DECREASE<br>`9` = TRANSACTION_CLOSE_IN<br>`10` = TRANSACTION_CLOSE_OUT<br>`11` = TRANSACTION_NEGATIVE_REVALUATION<br>`12` = TRANSACTION_NULLIFY<br>`13` = TRANSACTION_RESERVE_CI_IN<br>`14` = TRANSACTION_RESERVE_CI_OUT<br>`15` = TRANSACTION_RESERVE_CI_REVAL_INC<br>`16` = TRANSACTION_RESERVE_CI_REVAL_DEC<br>`17` = TRANSACTION_REVAL_PRICE_CHANGE_INCREASE<br>`18` = TRANSACTION_REVAL_PRICE_CHANGE_DECREASE |
| 16 | `ExpensesLC` | Expenses (LC) | Num | 19.6 | - |  |  |
| 17 | `ExpensesFC` | Expenses (FC) | Num | 19.6 | - |  |  |
| 18 | `ItemCode` | Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 19 | `DocDate` | Document Date | Date | 8 | - |  |  |
| 20 | `DocRate` | Document Rate | Num | 19.6 | - |  |  |
| 21 | `JrnlMemo` | Journal Remarks | nVarChar | 50 | - |  |  |
| 22 | `BaseLine` | Base Row Number | Int | 11 | - | -1 |  |
| 23 | `CreateTime` | Generation Time | Int | 6 | - |  |  |
| 24 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 25 | `OcrCode` | Distribution Rule | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 26 | `OcrCode2` | Distribution Rule2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 27 | `OcrCode3` | Distribution Rule3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 28 | `OcrCode4` | Distribution Rule4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 29 | `OcrCode5` | Distribution Rule5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 30 | `DocPrice` | Document Price | Num | 19.6 | - |  |  |
| 31 | `TreeType` | BOM Type | VarChar | 1 | - | N | `N` = Not a BOM<br>`A` = Assembly<br>`S` = Sales<br>`I` = BOM Component Item |
| 32 | `ApplObj` | Applied Object | Int | 11 | - | -1 |  |
| 33 | `AppObjAbs` | Applied Object Internal ID | Int | 11 | - | -1 |  |
| 34 | `AppObjType` | Applied Object Type | VarChar | 1 | - |  |  |
| 35 | `AppObjLine` | Applied Object Row | Int | 11 | - | -1 |  |
| 36 | `TransSeqRf` | Transaction Sequence Ref | Int | 11 | - | -1 |  |
| 37 | `LayerIDRef` | Layer ID Reference | Int | 11 | - | -1 |  |
| 38 | `VersionNum` | Version Number | nVarChar | 13 | - |  |  |
| 39 | `PriceRate` | Price Rate | Num | 19.6 | - |  |  |
| 40 | `PriceCurr` | Price Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 41 | `Price` | Price | Num | 19.6 | - |  |  |
| 42 | `CIShbQty` | Corr. Inv. Doc. Should Be Qty | Num | 19.6 | - |  |  |
| 43 | `SubLineNum` | Subrow Number | Int | 11 | - | -1 |  |
| 44 | `PrjCode` | Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 45 | `UseDocPric` | Use Document Price | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 46 | `Location` | Location | Int | 11 | [OLCT](OLCT.md) |  |  |
| 47 | `BSubLineNo` | Base Subrow Number | Int | 11 | - | -1 |  |
| 48 | `AppSubLine` | Applied Subrow Number | Int | 11 | - | -1 |  |
| 49 | `DocAction` | Document Action Type | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | MessageID |
