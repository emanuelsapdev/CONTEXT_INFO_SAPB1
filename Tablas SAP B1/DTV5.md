# DTV5 - Datev Run Errors Accounts

- **Tabla:** DTV5
- **Descripción:** Datev Run Errors Accounts
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DTV5.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `RunId` | Run Number | Int | 11 | [ODTV](ODTV.md) |  |  |
| 2 | `LineId` | Row Number | Int | 11 | - |  |  |
| 3 | `Confirm` | Confirmed | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 4 | `IntAccount` | Account Number | nVarChar | 15 | - |  |  |
| 5 | `Text` | Error Message | Text | 16 | - |  |  |
| 6 | `Detail` | Error Details | Text | 16 | - |  |  |
| 7 | `Type` | Error Type | VarChar | 1 | - |  | `E` = Error<br>`W` = Warning |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | RunId, LineId |
