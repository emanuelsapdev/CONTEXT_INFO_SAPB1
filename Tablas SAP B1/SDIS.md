# SDIS - Dynamic Interface (Strings)

- **Tabla:** SDIS
- **Descripción:** Dynamic Interface (Strings)
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SDIS.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `FormId` | Form ID | nVarChar | 40 | - |  |  |
| 2 | `ItemId` | Item ID | nVarChar | 40 | - |  |  |
| 3 | `ColumnId` | Column ID | nVarChar | 50 | - |  |  |
| 4 | `Language` | Language Code | Int | 11 | - | 0 |  |
| 5 | `ItemString` | Item String | nVarChar | 254 | - |  |  |
| 6 | `IsBold` | Is Bold | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `IsItalic` | Is Italics | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) | -1 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | FormId, ItemId, ColumnId, Language |
