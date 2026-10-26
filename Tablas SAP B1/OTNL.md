# OTNL - CCD Log

- **Tabla:** OTNL
- **Descripción:** CCD Log
- **Cantidad de campos:** 25
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OTNL.html

## Campos (25)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `TrNtAbsEnt` | Tracking Note Internal Number | Int | 11 | [OTCN](OTCN.md) |  |  |
| 3 | `TrNtLineNo` | Tracking Note Row Number | Int | 11 | [TCN1](TCN1.md) |  |  |
| 4 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 5 | `WhsCode` | Warehouse Code | nVarChar | 8 | - |  |  |
| 6 | `DocEntry` | Doc Abs Entry | Int | 11 | - |  |  |
| 7 | `DocNum` | Doc Number | Int | 11 | - |  |  |
| 8 | `DocType` | Transaction Type | Int | 11 | - | -1 |  |
| 9 | `DocLineNum` | Doc Line Number | Int | 11 | - |  |  |
| 10 | `BaseAbsEnt` | Base Abs Entry | Int | 11 | - | -1 |  |
| 11 | `BaseType` | Base Document Type | Int | 11 | - |  |  |
| 12 | `BaseLnNum` | Base Document Line No. | Int | 11 | - |  |  |
| 13 | `ActionType` | Action Type | Int | 11 | - | 5 | `0` = TRANSACTION_UNKNOWN<br>`1` = TRANSACTION_IN<br>`2` = TRANSACTION_OUT<br>`3` = TRANSACTION_SET<br>`4` = TRANSACTION_COMPLETE<br>`5` = EMPTY_TRANSACTION<br>`6` = TRANSACTION_REVALUATION<br>`7` = TRANSACTION_REVALUATION_INCREASE<br>`8` = TRANSACTION_REVALUATION_DECREASE<br>`9` = TRANSACTION_CLOSE_IN<br>`10` = TRANSACTION_CLOSE_OUT<br>`11` = TRANSACTION_NEGATIVE_REVALUATION<br>`12` = TRANSACTION_NULLIFY<br>`13` = TRANSACTION_RESERVE_CI_IN<br>`14` = TRANSACTION_RESERVE_CI_OUT<br>`15` = TRANSACTION_RESERVE_CI_REVAL_INC<br>`16` = TRANSACTION_RESERVE_CI_REVAL_DEC<br>`17` = TRANSACTION_REVAL_PRICE_CHANGE_INCREASE<br>`18` = TRANSACTION_REVAL_PRICE_CHANGE_DECREASE |
| 14 | `CCDNum` | CCD Number | nVarChar | 40 | - |  |  |
| 15 | `ItemCode` | Item Code | nVarChar | 50 | - |  |  |
| 16 | `DirectImp` | Direct Import | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 17 | `CntrOrigin` | Country/Region of Origin | nVarChar | 3 | - |  |  |
| 18 | `AccQty` | Quantity-In Accumulator | Num | 19.6 | - |  |  |
| 19 | `AccNegQ` | Quantity-Out Accumulator | Num | 19.6 | - |  |  |
| 20 | `AccRelQty` | Reallocation Quantity Accumulator | Num | 19.6 | - |  |  |
| 21 | `CCDQty` | CCD Quantity | Num | 19.6 | - |  |  |
| 22 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 23 | `CreateTime` | Generation Time | Int | 6 | - |  |  |
| 24 | `OnHandQty` | Warehouse On Hand Quantity | Num | 19.6 | - |  |  |
| 25 | `OILMEntry` | OILM Abs Entry | Int | 11 | [OILM](OILM.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
