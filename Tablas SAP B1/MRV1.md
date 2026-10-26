# MRV1 - Inventory Revaluation Information Array

- **Tabla:** MRV1
- **Descripción:** Inventory Revaluation Information Array
- **Cantidad de campos:** 23
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MRV1.html

## Campos (23)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [OMRV](OMRV.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `ItemCode` | Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 4 | `Dscription` | Item/Service Description | nVarChar | 200 | - |  |  |
| 5 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 6 | `Price` | Price | Num | 19.6 | - |  |  |
| 7 | `LineTotal` | Row Total | Num | 19.6 | - |  |  |
| 8 | `WhsCode` | Warehouse Code | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 9 | `RIncmAcct` | Inv. Reval. Increment Account | nVarChar | 15 | - |  |  |
| 10 | `RDcrmAcct` | Inv. Reval. Decrement Account | nVarChar | 15 | - |  |  |
| 11 | `RToStock` | Reval. Amount Posted to Stock | Num | 19.6 | - |  |  |
| 12 | `RActPrice` | Inv. Reval. Actual Price | Num | 19.6 | - |  |  |
| 13 | `ROnHand` | In Stock at Time of Revaluation | Num | 19.6 | - |  |  |
| 14 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 15 | `ObjType` | Object Type | nVarChar | 20 | - | 162 |  |
| 16 | `EvalSystem` | Cost Accounting Method | VarChar | 1 | [OITM](OITM.md) |  | `A` = Moving Average<br>`S` = Standard<br>`F` = FIFO<br>`B` = Serial/Batch |
| 17 | `OcrCode` | Distribution Rule | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 18 | `UnitMsr` | Unit of Measure | nVarChar | 100 | - |  |  |
| 19 | `OcrCode2` | Distribution Rule2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 20 | `OcrCode3` | Distribution Rule3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 21 | `OcrCode4` | Distribution Rule4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 22 | `OcrCode5` | Distribution Rule5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 23 | `Project` | Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum |
| ITEM_WHS | No | ItemCode, WhsCode |
| ITEM | No | ItemCode |
