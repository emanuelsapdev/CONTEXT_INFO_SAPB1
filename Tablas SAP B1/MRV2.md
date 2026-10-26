# MRV2 - Inventory Revaluation FIFO Rows

- **Tabla:** MRV2
- **Descripción:** Inventory Revaluation FIFO Rows
- **Cantidad de campos:** 21
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MRV2.html

## Campos (21)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [MRV1](MRV1.md) |  |  |
| 2 | `BaseLine` | Base Row Number | Int | 11 | - |  |  |
| 3 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 4 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 5 | `Price` | Price | Num | 19.6 | - |  |  |
| 6 | `LineTotal` | Row Total | Num | 19.6 | - |  |  |
| 7 | `RToStock` | Reval. Amount Posted to Stock | Num | 19.6 | - |  |  |
| 8 | `RActPrice` | Inventory Reval. Current Cost | Num | 19.6 | - |  |  |
| 9 | `INMTransNm` | INM Transaction Number | Int | 11 | [OINM](OINM.md) |  |  |
| 10 | `INMInst` | INM Instance | Int | 11 | [OINM](OINM.md) |  |  |
| 11 | `INMTransTy` | INM Transaction Type | Int | 11 | [OINM](OINM.md) | -1 |  |
| 12 | `INMCreatBy` | INM Document Key Created | Int | 11 | [OINM](OINM.md) |  |  |
| 13 | `INMBaseRef` | INM Base Reference | nVarChar | 11 | [OINM](OINM.md) |  |  |
| 14 | `INMDocDate` | INM Posting Date | Date | 8 | [OINM](OINM.md) |  |  |
| 15 | `INMOpenQty` | INM Open Quantity | Num | 19.6 | [OINM](OINM.md) |  |  |
| 16 | `ObjType` | Object Type | nVarChar | 20 | - | 162 |  |
| 17 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 18 | `IVLTransSe` | IVL Transaction Sequence No. | Int | 11 | - | -1 |  |
| 19 | `IVLLayerID` | IVL Layer ID | Int | 11 | - | -1 |  |
| 20 | `INMLineNum` | INM Row Number in Document | Int | 11 | [OINM](OINM.md) |  |  |
| 21 | `INMSubLine` | INM Subrow Number | Int | 11 | [OINM](OINM.md) | -1 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, BaseLine, LineNum |
