# SHR1 - Shareholder's Rights and Interests Report History - Rows

- **Tabla:** SHR1
- **Descripción:** Shareholder's Rights and Interests Report History - Rows
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SHR1.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ShrId` | SHR Identity | Int | 11 | [OSHR](OSHR.md) |  |  |
| 2 | `RowId` | Row Number | Int | 11 | - |  |  |
| 3 | `CatId` | Category Identity | Int | 6 | - |  |  |
| 4 | `LineNum` | Line Number | nVarChar | 6 | - |  |  |
| 5 | `ItemName` | Item Name | nVarChar | 254 | - |  |  |
| 6 | `Level` | Level Number | Int | 6 | - |  |  |
| 7 | `IndentChar` | Number of Characters to Indent | nVarChar | 6 | - |  |  |
| 8 | `Formula` | Formula? | VarChar | 1 | - |  |  |
| 9 | `CurAmount` | Current Period Amount | Num | 19.6 | - |  |  |
| 10 | `PreAmount` | Previous Period Amount | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ShrId, RowId |
