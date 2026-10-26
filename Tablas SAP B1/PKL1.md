# PKL1 - Pick List - Rows

- **Tabla:** PKL1
- **Descripción:** Pick List - Rows
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PKL1.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [OPKL](OPKL.md) |  |  |
| 2 | `PickEntry` | Row Number | Int | 11 | - |  |  |
| 3 | `OrderEntry` | Order Entry | Int | 11 | - |  |  |
| 4 | `OrderLine` | Order Row ID | Int | 11 | - |  |  |
| 5 | `PickQtty` | Picked Quantity | Num | 19.6 | - |  |  |
| 6 | `PickStatus` | Pick Status | VarChar | 1 | - | R | `R` = Released for Picking<br>`Y` = Picked<br>`P` = Partially Picked<br>`D` = Partially Delivered<br>`C` = Closed |
| 7 | `RelQtty` | Released Quantity | Num | 19.6 | - |  |  |
| 8 | `LogInsac` | Log Instance - History | Int | 11 | - |  |  |
| 9 | `PrevReleas` | Previously Released Quantity | Num | 19.6 | - |  |  |
| 10 | `BaseObject` | Base Object Type | Int | 11 | - |  | `17` = Order<br>`13` = Reserve Invoice<br>`202` = Production Order<br>`1250000001` = Inventory Transfer Request<br>`0` |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, PickEntry |
| ORDER | No | OrderEntry, OrderLine |
