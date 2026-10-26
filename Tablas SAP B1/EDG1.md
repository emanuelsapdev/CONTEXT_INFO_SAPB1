# EDG1 - Discount Groups Rows

- **Tabla:** EDG1
- **Descripción:** Discount Groups Rows
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/EDG1.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Unique Entry | Int | 11 | [OEDG](OEDG.md) |  |  |
| 2 | `ObjType` | Object Type | nVarChar | 20 | - |  | `52` = Item Groups<br>`8` = Item Properties<br>`43` = Manufacturer<br>`4` = Items |
| 3 | `ObjKey` | Object Key | nVarChar | 50 | - |  |  |
| 4 | `DiscType` | Discount Type | VarChar | 1 | - | D | `D` = Discount<br>`P` = Pay for/Get for Free |
| 5 | `Discount` | Discount | Num | 19.6 | - |  |  |
| 6 | `PayFor` | Paid Qty | Num | 19.6 | - |  |  |
| 7 | `ForFree` | Free Qty | Num | 19.6 | - |  |  |
| 8 | `UpTo` | Max. Free Qty | Num | 19.6 | - |  |  |
| 9 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, ObjType, ObjKey |
