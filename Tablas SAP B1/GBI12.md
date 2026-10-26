# GBI12 - GBI Row 12 - Shareholder's Rights and Interests Changing Report

- **Tabla:** GBI12
- **Descripción:** GBI Row 12 - Shareholder's Rights and Interests Changing Report
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/GBI12.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `HistoryId` | History Key | Int | 11 | [OGBI](OGBI.md) |  |  |
| 2 | `RowId` | Row Number | Int | 11 | - |  |  |
| 3 | `ShrId` | SHR Report History ID | Int | 11 | - |  |  |
| 4 | `RowNum` | Row Number in Saved Report | Int | 11 | - |  |  |
| 5 | `ItemName` | Item Name | nVarChar | 254 | - |  |  |
| 6 | `LineNum` | Line number | nVarChar | 6 | - |  |  |
| 7 | `CurAmount` | Amount for Current Period | Num | 19.6 | - |  |  |
| 8 | `PreAmount` | Amount for Previous Period | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | HistoryId, RowId |
