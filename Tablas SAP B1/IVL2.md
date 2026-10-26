# IVL2 - Inventory Components for Production

- **Tabla:** IVL2
- **Descripción:** Inventory Components for Production
- **Cantidad de campos:** 18
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/IVL2.html

## Campos (18)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Transseq` | Transaction sequence | Int | 11 | - |  |  |
| 2 | `MessageID` | Message ID | Int | 11 | [OILM](OILM.md) |  |  |
| 3 | `LineID` | Line ID | Int | 11 | - |  |  |
| 4 | `POLine` | Line in Production Order | Int | 11 | - |  |  |
| 5 | `ItemType` | Item Type | Int | 11 | - |  |  |
| 6 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 7 | `LocType` | Location Type | Int | 6 | - |  |  |
| 8 | `LocCode` | Location Code | nVarChar | 8 | - |  |  |
| 9 | `LayerTSeq` | FIFO Layer Transaction Sequence | Int | 11 | - | -1 |  |
| 10 | `LayerId` | Layer ID | Int | 11 | - | -1 |  |
| 11 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 12 | `TotalLC` | Inventory Total LC | Num | 19.6 | - |  |  |
| 13 | `BaseAbsEnt` | Abs. Entry of Base Doc. | Int | 11 | - | -1 |  |
| 14 | `BaseType` | Base Transaction Type | Int | 11 | - | -1 | `-1`<br>`0`<br>`60` = Goods Issue |
| 15 | `BaseLine` | Base Line Number | Int | 11 | - | -1 |  |
| 16 | `StgSeqNum` | Stage Sequence Number | Int | 11 | - |  |  |
| 17 | `StgEntry` | Stage Entry | Int | 11 | [ORST](ORST.md) |  |  |
| 18 | `StgDesc` | Stage Description | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | MessageID, LineID |
