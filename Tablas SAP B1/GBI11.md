# GBI11 - GBI Row 11 - Devalue Provision of Enterprise Assets

- **Tabla:** GBI11
- **Descripción:** GBI Row 11 - Devalue Provision of Enterprise Assets
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/GBI11.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `HistoryId` | History ID | Int | 11 | [OGBI](OGBI.md) |  |  |
| 2 | `RowId` | Row Number | Int | 11 | - |  |  |
| 3 | `ItemName` | Item Name | nVarChar | 100 | - |  |  |
| 4 | `BOPBalance` | Balance at Beginning of Period | Num | 19.6 | - |  |  |
| 5 | `CurDebit` | Current Period in Debit | Num | 19.6 | - |  |  |
| 6 | `CurCredit` | Current Period in Credit | Num | 19.6 | - |  |  |
| 7 | `EOPBalance` | Balance at End of Period | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | HistoryId, RowId |
