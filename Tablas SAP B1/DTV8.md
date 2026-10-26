# DTV8 - Datev Run Configuration

- **Tabla:** DTV8
- **Descripción:** Datev Run Configuration
- **Cantidad de campos:** 13
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DTV8.html

## Campos (13)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `RunId` | Run Number | Int | 11 | [ODTV](ODTV.md) |  |  |
| 2 | `LineId` | Row Number | Int | 11 | - |  |  |
| 3 | `ConsId` | Advisor Number | Int | 11 | - |  |  |
| 4 | `ConsName` | Advisor Name | nVarChar | 100 | - |  |  |
| 5 | `ClientId` | Client Number | Int | 11 | - |  |  |
| 6 | `DFVCode` | DFV Code | nVarChar | 50 | - |  |  |
| 7 | `Curr` | Currency | nVarChar | 10 | - |  |  |
| 8 | `GLLength` | Account Number Length | Int | 11 | - |  |  |
| 9 | `IntAcc` | Temporary Account | nVarChar | 15 | - |  |  |
| 10 | `IntTax` | Tax Temporary Account | nVarChar | 15 | - |  |  |
| 11 | `SetOfBoks` | Chart of Accounts | nVarChar | 15 | - |  |  |
| 12 | `CostDim` | Cost Center Dimension | nVarChar | 15 | - |  |  |
| 13 | `FormatVer` | Format Version | nVarChar | 10 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | RunId, LineId |
