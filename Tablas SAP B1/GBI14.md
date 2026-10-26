# GBI14 - GBI Row 14 - Small Enterprise's Cash Flow Statement

- **Tabla:** GBI14
- **Descripción:** GBI Row 14 - Small Enterprise's Cash Flow Statement
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/GBI14.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `HistoryId` | History Key | Int | 11 | [OGBI](OGBI.md) |  |  |
| 2 | `RowId` | Row Number | Int | 11 | - |  |  |
| 3 | `LineTitle` | Line Title | nVarChar | 100 | - |  |  |
| 4 | `LineNum` | Line Number | nVarChar | 5 | - |  |  |
| 5 | `PreAmount` | Previous Year Amount | Num | 19.6 | - |  |  |
| 6 | `CurAmount` | Current Year Amount | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | HistoryId, RowId |
