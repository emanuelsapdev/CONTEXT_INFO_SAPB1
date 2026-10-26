# OSLR - Special Ledger - Analytical Accounting Report: Revenues & Expenses

- **Tabla:** OSLR
- **Descripción:** Special Ledger - Analytical Accounting Report: Revenues & Expenses
- **Cantidad de campos:** 15
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSLR.html

## Campos (15)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocID` | Document Identification Number | Int | 11 | - |  |  |
| 2 | `DocDate` | Date of Report Generation | Date | 8 | - |  |  |
| 3 | `Ref1` | Journal Entry Number | Int | 11 | [OJDT](OJDT.md) |  |  |
| 4 | `Ref2` | Original JE Reference | Int | 11 | [OJDT](OJDT.md) |  |  |
| 5 | `Status` | Document Status | VarChar | 1 | - |  |  |
| 6 | `DateFrom` | Document Start Date | Date | 8 | - |  |  |
| 7 | `DateTo` | Document End Date | Date | 8 | - |  |  |
| 8 | `TotDebit` | Total Debit Amount | Num | 19.6 | - |  |  |
| 9 | `TotCredit` | Total Credit Amount | Num | 19.6 | - |  |  |
| 10 | `RateType` | Type of Exchange Rate | VarChar | 1 | - | O | `O` = Original document<br>`E` = Execution date<br>`V` = Other value |
| 11 | `Comment` | Remarks | nVarChar | 250 | - |  |  |
| 12 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 13 | `Canceled` | Canceled | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 14 | `CancelDate` | Cancelation Date | Date | 8 | - |  |  |
| 15 | `CancelUser` | Document Cancelled by | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocID |
