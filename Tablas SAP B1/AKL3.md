# AKL3 - Pick List for SnB and Bin Delivered Details

- **Tabla:** AKL3
- **Descripción:** Pick List for SnB and Bin Delivered Details
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AKL3.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [OPKL](OPKL.md) |  |  |
| 2 | `PickEntry` | Row Number | Int | 11 | - |  |  |
| 3 | `Pkl3LinNum` | PKL3 Line Number | Int | 11 | - |  |  |
| 4 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 5 | `ManagedBy` | Management Method | Int | 11 | - | -1 | `10000044` = BTN<br>`10000045` = SRN<br>`-1` = NOB |
| 6 | `SnBEntry` | SnB Abs. Entry | Int | 11 | - |  |  |
| 7 | `BinAbs` | Bin Internal Number | Int | 11 | [OBIN](OBIN.md) |  |  |
| 8 | `AllowNeg` | Allow Negative Entry [Y/N] | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 9 | `RelQtty` | Released Quantity | Num | 19.6 | - |  |  |
| 10 | `PickQtty` | Picked Quantity | Num | 19.6 | - |  |  |
| 11 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 156 |  |
| 12 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, PickEntry, Pkl3LinNum, LogInstanc |
