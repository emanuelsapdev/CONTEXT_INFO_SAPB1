# DTV4 - Datev Run Errors

- **Tabla:** DTV4
- **Descripción:** Datev Run Errors
- **Cantidad de campos:** 7
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DTV4.html

## Campos (7)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `RunId` | Run Number | Int | 11 | [ODTV](ODTV.md) |  |  |
| 2 | `LineId` | Row Number | Int | 11 | - |  |  |
| 3 | `Confirm` | Confirmed | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 4 | `JourlEntry` | Journal Entry | Int | 11 | - |  |  |
| 5 | `Text` | Error Message | Text | 16 | - |  |  |
| 6 | `Detail` | Error Details | Text | 16 | - |  |  |
| 7 | `Type` | Error Type | VarChar | 1 | - |  | `E` = Error<br>`W` = Warning |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | RunId, LineId |
