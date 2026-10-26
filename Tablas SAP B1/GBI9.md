# GBI9 - GBI Row 9 - Enterprise's Profit and Loss Statement

- **Tabla:** GBI9
- **Descripción:** GBI Row 9 - Enterprise's Profit and Loss Statement
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/GBI9.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `HistoryId` | History Key | Int | 11 | [OGBI](OGBI.md) |  |  |
| 2 | `RowId` | Row Number | Int | 11 | - |  |  |
| 3 | `RepItm` | Report Item | nVarChar | 60 | - |  |  |
| 4 | `RepItmNo` | Report Item Number | nVarChar | 3 | - |  |  |
| 5 | `PeriodAmt` | Period Amount | Num | 19.6 | - |  |  |
| 6 | `YearAmt` | Year Accumulated Amount | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | HistoryId, RowId |
