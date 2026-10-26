# UIVE - FIFO Based Sales Return

- **Tabla:** UIVE
- **Descripción:** FIFO Based Sales Return
- **Cantidad de campos:** 13
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UIVE.html

## Campos (13)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TreeID` | Tree ID | Int | 11 | - | 0 |  |
| 2 | `ParentID` | Parent ID | Int | 11 | - | -1 |  |
| 3 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 4 | `LocType` | Location Type | Int | 6 | - |  |  |
| 5 | `LocCode` | Location Code | nVarChar | 8 | - |  |  |
| 6 | `TransSeq` | Transaction Sequence No. | Int | 11 | [UIVL](UIVL.md) |  |  |
| 7 | `LayerID` | Layer ID | Int | 11 | - |  |  |
| 8 | `LayerInQty` | Layer In Quantity | Num | 19.6 | - |  |  |
| 9 | `LayerOutQ` | Layer Out Quantity | Num | 19.6 | - |  |  |
| 10 | `LayerVal` | Layer Value | Num | 19.6 | - |  |  |
| 11 | `ItemCode` | Item Code | nVarChar | 50 | [UITM](UITM.md) |  |  |
| 12 | `EntryTreeI` | Entry Tree ID | Int | 11 | - |  |  |
| 13 | `LayerCogs` | Layer - Cost of Goods Sold | Num | 19.6 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| TRANS_SEQ | No | TransSeq, LayerID |
| TreeID | No | TreeID |
