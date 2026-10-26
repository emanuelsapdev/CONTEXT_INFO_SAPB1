# UBVL - Serial Numbers and Batch Valuation Log

- **Tabla:** UBVL
- **Descripción:** Serial Numbers and Batch Valuation Log
- **Cantidad de campos:** 36
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UBVL.html

## Campos (36)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `DocEntry` | Doc. Abs. Entry | Int | 11 | - |  |  |
| 3 | `DocLineNum` | Doc. Line Number | Int | 11 | - |  |  |
| 4 | `DocType` | Transact. Type | Int | 11 | - | -1 |  |
| 5 | `BaseType` | Base Document Type | Int | 11 | - | -1 | `-1`<br>`0`<br>`13` = A/R Invoice<br>`15` = Delivery<br>`16` = Returns<br>`17` = Sales Order<br>`18` = A/P Invoice<br>`20` = Goods Receipt PO<br>`21` = Goods Return<br>`22` = Purchase Order<br>`23` = Sales Quotation<br>`59` = Goods Receipt<br>`67` = Inventory Transfer<br>`69` = Landed Costs<br>`163` = A/P Correction Invoice<br>`164` = A/P Correction Invoice Reversal<br>`165` = A/R Correction Invoice<br>`166` = A/R Correction Invoice Reversal<br>`202` = Production Order<br>`203` = A/R Down Payment<br>`204` = A/P Down Payment |
| 6 | `ActionType` | Action Type | Int | 11 | - | 5 | `0` = TRANSACTION_UNKNOWN<br>`1` = TRANSACTION_IN<br>`2` = TRANSACTION_OUT<br>`3` = TRANSACTION_SET<br>`4` = TRANSACTION_COMPLETE<br>`5` = EMPTY_TRANSACTION<br>`6` = TRANSACTION_REVALUATION<br>`7` = TRANSACTION_REVALUATION_INCREASE<br>`8` = TRANSACTION_REVALUATION_DECREASE<br>`9` = TRANSACTION_CLOSE_IN<br>`10` = TRANSACTION_CLOSE_OUT<br>`11` = TRANSACTION_NEGATIVE_REVALUATION<br>`12` = TRANSACTION_NULLIFY<br>`13` = TRANSACTION_RESERVE_CI_IN<br>`14` = TRANSACTION_RESERVE_CI_OUT<br>`15` = TRANSACTION_RESERVE_CI_REVAL_INC<br>`16` = TRANSACTION_RESERVE_CI_REVAL_DEC<br>`17` = TRANSACTION_REVAL_PRICE_CHANGE_INCREASE<br>`18` = TRANSACTION_REVAL_PRICE_CHANGE_DECREASE |
| 7 | `AccumType` | Accumulator Type | Int | 11 | - | 0 | `0` = ACCUM_EMPTY<br>`1` = ACCUM_ON_HAND<br>`2` = ACCUM_COMMITTED<br>`3` = ACCUM_ON_ORDER<br>`4` = ACCUM_CONSIGNATION<br>`5` = ACCUM_COUNTED |
| 8 | `ManagedBy` | Managed By | Int | 11 | - | -1 | `10000044` = Batch Numbers<br>`10000045` = Serial Numbers |
| 9 | `CreateDate` | Generation Date | Date | 8 | - |  |  |
| 10 | `CreateTime` | Generation Time | Int | 6 | - |  |  |
| 11 | `ItemCode` | Item No. | nVarChar | 50 | - |  |  |
| 12 | `SysNumber` | System Number | Int | 11 | - |  |  |
| 13 | `DistNumber` | Batch Number | nVarChar | 36 | - |  |  |
| 14 | `MdAbsEntry` | MD Abs. Entry | Int | 11 | - |  |  |
| 15 | `TrValApply` | Apply Transaction Value | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 16 | `TransValue` | Transaction Value | Num | 19.6 | - |  |  |
| 17 | `InvValue` | Inventory Value | Num | 19.6 | - |  |  |
| 18 | `CogsValue` | Cogs Value | Num | 19.6 | - |  |  |
| 19 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 20 | `OverlapQty` | Overlap Quantity | Num | 19.6 | - |  |  |
| 21 | `CogsQty` | Cogs Quantity | Num | 19.6 | - |  |  |
| 22 | `CalcPrice` | Calculated Price | Num | 19.6 | - |  |  |
| 23 | `PriceDiff` | Price Difference | Num | 19.6 | - |  |  |
| 24 | `InvDiff` | Inventory Difference | Num | 19.6 | - |  |  |
| 25 | `Balance` | Batch Balance | Num | 19.6 | - |  |  |
| 26 | `AccTotal` | Total Accumulator | Num | 19.6 | - |  |  |
| 27 | `AccQty` | Quantity-Out Accumulator | Num | 19.6 | - |  |  |
| 28 | `AccNegQ` | Quantity-In Accumulator | Num | 19.6 | - |  |  |
| 29 | `ILMEntry` | ILM Entry | Int | 11 | - |  |  |
| 30 | `ITLEntry` | ITL Entry | Int | 11 | - |  |  |
| 31 | `CostQty` | Cost Quantity | Num | 19.6 | - |  |  |
| 32 | `Cost` | Cost | Num | 19.6 | - |  |  |
| 33 | `BaseDocEn` | Base Doc. Abs. Entry | Int | 11 | - |  |  |
| 34 | `BaseLnNum` | Base Doc. Line Number | Int | 11 | - |  |  |
| 35 | `DeltaAccT` | Delta Total Accumulator | Num | 19.6 | - |  |  |
| 36 | `RowAction` | Row Action Type | Int | 11 | - |  | `0` = TRANSACTION_UNKNOWN<br>`1` = TRANSACTION_IN<br>`2` = TRANSACTION_OUT<br>`3` = TRANSACTION_SET<br>`4` = TRANSACTION_COMPLETE<br>`5` = EMPTY_TRANSACTION<br>`6` = TRANSACTION_REVALUATION<br>`7` = TRANSACTION_REVALUATION_INCREASE<br>`8` = TRANSACTION_REVALUATION_DECREASE<br>`9` = TRANSACTION_CLOSE_IN<br>`10` = TRANSACTION_CLOSE_OUT<br>`11` = TRANSACTION_NEGATIVE_REVALUATION<br>`12` = TRANSACTION_NULLIFY<br>`13` = TRANSACTION_RESERVE_CI_IN<br>`14` = TRANSACTION_RESERVE_CI_OUT<br>`15` = TRANSACTION_RESERVE_CI_REVAL_INC<br>`16` = TRANSACTION_RESERVE_CI_REVAL_DEC<br>`17` = TRANSACTION_REVAL_PRICE_CHANGE_INCREASE<br>`18` = TRANSACTION_REVAL_PRICE_CHANGE_DECREASE |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
