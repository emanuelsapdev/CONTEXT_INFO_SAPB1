# AIT11 - Asset Item Period Control

- **Tabla:** AIT11
- **Descripción:** Asset Item Period Control
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AIT11.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ItemCode` | Item No. | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 2 | `PeriodCat` | Period Category | nVarChar | 10 | - |  |  |
| 3 | `DprArea` | Depreciation Area | nVarChar | 15 | [ODPA](ODPA.md) |  |  |
| 4 | `VisOrder` | Visual Order | Int | 11 | - |  |  |
| 5 | `DprSt` | Depreciation Status | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 6 | `factor` | Factor | Num | 19.6 | - |  |  |
| 7 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 8 | `ActualUnit` | Actual Units | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ItemCode, PeriodCat, DprArea, VisOrder, LogInstanc |
