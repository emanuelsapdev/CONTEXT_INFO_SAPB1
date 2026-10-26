# GBI6 - GBI Row 6 - G/L Account Balance

- **Tabla:** GBI6
- **Descripción:** GBI Row 6 - G/L Account Balance
- **Cantidad de campos:** 18
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/GBI6.html

## Campos (18)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `HistoryId` | History Key | Int | 11 | [OGBI](OGBI.md) |  |  |
| 2 | `RowId` | Row Number | Int | 11 | - |  |  |
| 3 | `AcctCode` | Account Code | nVarChar | 15 | - |  |  |
| 4 | `Currency` | Account Currency | nVarChar | 3 | - |  |  |
| 5 | `EvalGrp` | Group for Calculating | nVarChar | 254 | - |  |  |
| 6 | `PerBBal` | Period Begin Balance | Num | 19.6 | - |  |  |
| 7 | `PerBQty` | Period Begin Quantity | Num | 19.6 | - |  |  |
| 8 | `PerBFCBal` | Period Begin FC Balance | Num | 19.6 | - |  |  |
| 9 | `CPDAmt` | Current Period Debit Amount | Num | 19.6 | - |  |  |
| 10 | `CPDQty` | Current Period Debit Quantity | Num | 19.6 | - |  |  |
| 11 | `CPDFCAmt` | Current Period Debit FC Amount | Num | 19.6 | - |  |  |
| 12 | `CPCAmt` | Current Period Credit Amount | Num | 19.6 | - |  |  |
| 13 | `CPCQty` | Current Period Credit Quantity | Num | 19.6 | - |  |  |
| 14 | `CPCFCAmt` | Current Period Credit FC Amnt | Num | 19.6 | - |  |  |
| 15 | `PerEBal` | Period End Balance | Num | 19.6 | - |  |  |
| 16 | `PerEQty` | Period End Quantity | Num | 19.6 | - |  |  |
| 17 | `PerEFCBal` | Period End FC Balance | Num | 19.6 | - |  |  |
| 18 | `AcctPeriod` | Fiscal Month | nVarChar | 2 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | HistoryId, RowId |
