# GBI13 - GBI Row 13 - Enterprise's Profit Distribution Report

- **Tabla:** GBI13
- **Descripción:** GBI Row 13 - Enterprise's Profit Distribution Report
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/GBI13.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `HistoryId` | History ID | Int | 11 | [OGBI](OGBI.md) |  |  |
| 2 | `RowId` | Row Number | Int | 11 | - |  |  |
| 3 | `ItemName` | Item Name | nVarChar | 100 | - |  |  |
| 4 | `LineNum` | Line Number | nVarChar | 6 | - |  |  |
| 5 | `CurAmount` | Current Period Amount | Num | 19.6 | - |  |  |
| 6 | `PreAmount` | Previous Period Amount | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | HistoryId, RowId |
