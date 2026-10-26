# OBAL - Opening Balances

- **Tabla:** OBAL
- **Descripción:** Opening Balances
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBAL.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 3 | `WhsCode` | Warehouse Code | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 4 | `PeriodID` | Period Indicator | Int | 11 | [BAL2](BAL2.md) |  |  |
| 5 | `EvalSystem` | Valuation Method | VarChar | 1 | - | W | `A` = Moving Average<br>`F` = FIFO<br>`W` = Weighted Average |
| 6 | `DtSorting` | Date Sorting Method | VarChar | 1 | - | P | `S` = System Date<br>`P` = Posting Date<br>`E` = Effective Posting Date |
| 7 | `LayerID` | Layer ID | Int | 11 | - | -1 |  |
| 8 | `CreateDate` | Create Date | Date | 8 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| SECONDARY | Yes | ItemCode, WhsCode, PeriodID, EvalSystem, DtSorting, LayerID |
