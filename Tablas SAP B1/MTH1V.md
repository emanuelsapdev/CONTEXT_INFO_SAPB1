# MTH1V - Journal Entries of External Reconciliation

- **Tabla:** MTH1V
- **Descripción:** Journal Entries of External Reconciliation
- **Cantidad de campos:** 18
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MTH1V.html

## Campos (18)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `MthAcctCod` | Account Code | nVarChar | 15 | - |  |  |
| 2 | `IsInternal` | Reconciliation Type | VarChar | 1 | - | E | `I` = Internal<br>`E` = External |
| 3 | `MatchNum` | Reconciliation No. | Int | 11 | - |  |  |
| 4 | `TransID` | Transaction No. | Int | 11 | - |  |  |
| 5 | `Line_ID` | Row Number | Int | 11 | - |  |  |
| 6 | `RefDate` | Posting Date | Date | 8 | - |  |  |
| 7 | `DueDate` | Due Date | Date | 8 | - |  |  |
| 8 | `Ref1` | Reference 1 | nVarChar | 200 | - |  |  |
| 9 | `Ref2` | Reference 2 | nVarChar | 200 | - |  |  |
| 10 | `Ref3Line` | Reference 3 | nVarChar | 200 | - |  |  |
| 11 | `Debit` | Debit Amount | Num | 19.6 | - |  |  |
| 12 | `Credit` | Credit Amount | Num | 19.6 | - |  |  |
| 13 | `SYSDeb` | System Debit Amount | Num | 19.6 | - |  |  |
| 14 | `SYSCred` | System Credit Amount | Num | 19.6 | - |  |  |
| 15 | `FCDebit` | Foreign Debit Amount | Num | 19.6 | - |  |  |
| 16 | `FCCredit` | Foreign Credit Amount | Num | 19.6 | - |  |  |
| 17 | `Currency` | Currency | nVarChar | 3 | - |  |  |
| 18 | `LineMemo` | Row Details | nVarChar | 254 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | MthAcctCod, IsInternal, MatchNum, TransID, Line_ID |
