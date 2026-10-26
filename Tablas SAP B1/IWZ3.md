# IWZ3 - Items Last Revaluation Data

- **Tabla:** IWZ3
- **Descripción:** Items Last Revaluation Data
- **Cantidad de campos:** 16
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/IWZ3.html

## Campos (16)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | [OIWZ](OIWZ.md) |  |  |
| 2 | `ItemCode` | Item Number | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 3 | `WhCode` | Warehouse Code | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 4 | `RevalPrice` | Revaluated Price | Num | 19.6 | - |  |  |
| 5 | `BaseCurr` | Item Base Currency | nVarChar | 3 | - |  |  |
| 6 | `RevalDate` | Revaluation Date | Date | 8 | - |  |  |
| 7 | `RevalSum` | Revaluation Sum | Num | 19.6 | - |  |  |
| 8 | `BasePrice` | Base Price | Num | 19.6 | - |  |  |
| 9 | `RealAcct` | Revaluation Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 10 | `RevalOfsac` | Reval. Offset Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 11 | `RevalType` | Revaluation Type | VarChar | 1 | - | S | `S` = Inventory Reval. Type<br>`C` = COGS Revaluation Type |
| 12 | `ExeLine` | Executed Row | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 13 | `RevCancel` | Revaluation Cancel | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 14 | `RvCaclDate` | Reval. Acct Cancellation Date | Date | 8 | - |  |  |
| 15 | `Quantity` | Quantity | Num | 19.6 | - |  |  |
| 16 | `BalanceBef` | Balance Before Revaluation | Num | 19.6 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, ItemCode, WhCode |
| ABS | No | AbsEntry |
