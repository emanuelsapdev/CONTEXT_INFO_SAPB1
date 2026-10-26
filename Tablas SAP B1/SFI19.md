# SFI19 - Self Invoice - Bin Allocation Data

- **Tabla:** SFI19
- **Descripción:** Self Invoice - Bin Allocation Data
- **Cantidad de campos:** 14
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SFI19.html

## Campos (14)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | [OSFI](OSFI.md) |  |  |
| 2 | `BinAllocSe` | Bin Allocation Sequence | Int | 11 | - |  |  |
| 3 | `LineNum` | Line Number | Int | 11 | - |  |  |
| 4 | `SubLineNum` | Subline Number | Int | 11 | - | -1 |  |
| 5 | `SnBType` | SnB Type | Int | 11 | - | -1 |  |
| 6 | `SnBMDAbs` | SnB Master Data Internal No. | Int | 11 | - | -1 |  |
| 7 | `BinAbs` | Bin Internal Number | Int | 11 | [OBIN](OBIN.md) |  |  |
| 8 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 9 | `ItemCode` | Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 10 | `WhsCode` | Warehouse Code | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 11 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 254000065 |  |
| 12 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 13 | `AllowNeg` | Allow Negative Entry [Y/N] | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 14 | `BinActTyp` | Bin Action Type | Int | 6 | - |  | `1` = Transaction In<br>`2` = Transaction Out<br>`4` = SnB Complete<br>`8` = Bin First Then SnB |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, BinAllocSe |
