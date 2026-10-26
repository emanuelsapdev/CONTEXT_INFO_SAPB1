# DTV2 - Datev Run Lines Accounts

- **Tabla:** DTV2
- **Descripción:** Datev Run Lines Accounts
- **Cantidad de campos:** 5
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DTV2.html

## Campos (5)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `RunId` | Run Number | Int | 11 | [ODTV](ODTV.md) |  |  |
| 2 | `LineId` | Row Number | Int | 11 | - |  |  |
| 3 | `IntAccount` | Account Number | nVarChar | 15 | - |  |  |
| 4 | `Text` | Run results | Text | 16 | - |  |  |
| 5 | `Detail` | Run Details | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | RunId, LineId |
