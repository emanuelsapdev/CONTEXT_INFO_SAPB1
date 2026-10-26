# DTV6 - Datev Run Errors Cards

- **Tabla:** DTV6
- **Descripción:** Datev Run Errors Cards
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DTV6.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `RunId` | Run Number | Int | 11 | [ODTV](ODTV.md) |  |  |
| 2 | `LineId` | Row Number | Int | 11 | - |  |  |
| 3 | `CardCode` | Customer Number | nVarChar | 50 | - |  |  |
| 4 | `CardName` | Customer Name | nVarChar | 100 | - |  |  |
| 5 | `Confirm` | Confirmed | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `Text` | Error Message | Text | 16 | - |  |  |
| 7 | `CardType` | Customer Type | VarChar | 1 | - |  | `C` = Customer<br>`S` = Supplier |
| 8 | `Detail` | Error Details | Text | 16 | - |  |  |
| 9 | `Type` | Error Type | VarChar | 1 | - |  | `E` = Error<br>`W` = Warning |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | RunId, LineId |
