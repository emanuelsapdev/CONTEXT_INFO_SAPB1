# GBI8 - GBI Row 8 - Enterprise's Balance Sheet

- **Tabla:** GBI8
- **Descripción:** GBI Row 8 - Enterprise's Balance Sheet
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/GBI8.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `HistoryId` | History Key | Int | 11 | [OGBI](OGBI.md) |  |  |
| 2 | `RowId` | Row Number | Int | 11 | - |  |  |
| 3 | `AcctName` | Account Name | nVarChar | 200 | - |  |  |
| 4 | `LineNum` | Line Number | nVarChar | 6 | - |  |  |
| 5 | `YearBAmt` | Year Begin Amount | Num | 19.6 | - |  |  |
| 6 | `PerEAmt` | Period End Amount | Num | 19.6 | - |  |  |
| 7 | `RepDate` | Report Date | nVarChar | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | HistoryId, RowId |
