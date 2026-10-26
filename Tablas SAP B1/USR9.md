# USR9 - User Print Log

- **Tabla:** USR9
- **Descripción:** User Print Log
- **Cantidad de campos:** 13
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/USR9.html

## Campos (13)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocCode` | Code | nVarChar | 8 | - |  |  |
| 2 | `DocName` | Name | nVarChar | 120 | - |  |  |
| 3 | `UserCode` | User Code | nVarChar | 25 | [OUSR](OUSR.md) |  |  |
| 4 | `Action` | Performed Action | VarChar | 1 | - |  | `P` = Print<br>`E` = Export |
| 5 | `ActionBy` | User Who Performed the Action | nVarChar | 25 | - |  |  |
| 6 | `SessionID` | Connection Session ID | Int | 11 | - | -1 |  |
| 7 | `Date` | Date | Date | 8 | - |  |  |
| 8 | `Time` | Time | Int | 11 | - | 0 |  |
| 9 | `DocType` | Document Type | nVarChar | 200 | - |  |  |
| 10 | `DocNum` | Document Number | Int | 11 | - | -1 |  |
| 11 | `NCopies` | Number of Copies | Int | 11 | - | 0 |  |
| 12 | `Printer` | Printer Name | nVarChar | 200 | - |  |  |
| 13 | `UserID` | User ID | Int | 6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | UserCode, Action, Date, Time, SessionID |
