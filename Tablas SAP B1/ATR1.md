# ATR1 - Transportation Document Lines - History

- **Tabla:** ATR1
- **Descripción:** Transportation Document Lines - History
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ATR1.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [ATRO](ATRO.md) |  |  |
| 2 | `LineNum` | Line Number | Int | 11 | - |  |  |
| 3 | `DocObjType` | Document Object Type | Int | 11 | - |  | `13` = A/R Invoice<br>`15` = Delivery<br>`21` = Goods Return<br>`67` = Inventory Transfer |
| 4 | `DocEntry` | Internal Number | Int | 11 | - |  |  |
| 5 | `DocLineNum` | Document Line Number | Int | 11 | - |  |  |
| 6 | `ItemCode` | Item No. | nVarChar | 50 | - |  |  |
| 7 | `TranspQty` | Transported Quantity | Num | 19.6 | - |  |  |
| 8 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 9 | `DocOrdNum` | Document Order Number | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineNum, LogInstanc |
