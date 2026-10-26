# UILM3 - Non-Inventory and Resource Components Log Msg

- **Tabla:** UILM3
- **Descripción:** Non-Inventory and Resource Components Log Msg
- **Cantidad de campos:** 15
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UILM3.html

## Campos (15)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `MessageID` | Message ID | Int | 11 | [OILM](OILM.md) |  |  |
| 2 | `LineID` | Line ID | Int | 11 | - |  |  |
| 3 | `POLine` | Line in Production Order | Int | 11 | - |  |  |
| 4 | `ItemType` | Item Type | Int | 11 | - |  |  |
| 5 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 6 | `LocType` | Location Type | Int | 6 | - |  |  |
| 7 | `LocCode` | Location Code | nVarChar | 8 | - |  |  |
| 8 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 9 | `TotalLC` | Inventory Total LC | Num | 19.6 | - |  |  |
| 10 | `BaseAbsEnt` | Abs. Entry of Base Doc. | Int | 11 | - | -1 |  |
| 11 | `BaseType` | Base Transaction Type | Int | 11 | - | -1 | `-1`<br>`0`<br>`60` = Goods Issue |
| 12 | `BaseLine` | Base Line Number | Int | 11 | - | -1 |  |
| 13 | `StgSeqNum` | Stage Sequence Number | Int | 11 | - |  |  |
| 14 | `StgEntry` | Stage Entry | Int | 11 | - |  |  |
| 15 | `StgDesc` | Stage Description | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | MessageID, ItemCode, LineID |
