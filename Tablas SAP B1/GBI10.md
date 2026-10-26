# GBI10 - GBI Row 10 - Enterprise's Cash Flow Statement

- **Tabla:** GBI10
- **Descripción:** GBI Row 10 - Enterprise's Cash Flow Statement
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/GBI10.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `HistoryId` | History Key | Int | 11 | [OGBI](OGBI.md) |  |  |
| 2 | `RowId` | Row Number | Int | 11 | - |  |  |
| 3 | `LineTitle` | Line Title | nVarChar | 100 | - |  |  |
| 4 | `LineNum` | Line Number | nVarChar | 5 | - |  |  |
| 5 | `Amount` | Amount | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | HistoryId, RowId |
