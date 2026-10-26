# SDEX - Dynamic Extensions

- **Tabla:** SDEX
- **Descripción:** Dynamic Extensions
- **Cantidad de campos:** 8
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SDEX.html

## Campos (8)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `FormId` | Form ID | Int | 11 | - |  |  |
| 2 | `ItemId` | Item ID | Int | 11 | - | 0 |  |
| 3 | `ColumnId` | Column ID | Int | 11 | - | 0 |  |
| 4 | `BefAppl` | Application Before | Text | 16 | - |  |  |
| 5 | `AftAppl` | Application After | Text | 16 | - |  |  |
| 6 | `BefScript` | Is Script Before | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 7 | `AftScript` | Is Script After | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 8 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) | -1 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | FormId, ItemId, ColumnId |
