# RTM1 - Rate Differences - Rows

- **Tabla:** RTM1
- **Descripción:** Rate Differences - Rows
- **Cantidad de campos:** 19
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RTM1.html

## Campos (19)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `LineNum` | Reconciliation Key | Int | 11 | - |  |  |
| 2 | `TransId` | Journal Key | Int | 11 | [OJDT](OJDT.md) |  |  |
| 3 | `JdtLine` | Journal Row | Int | 11 | - | 0 |  |
| 4 | `IsSysCurr` | Is System Currency | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `AcctCode` | G/L Account/BP Code | nVarChar | 15 | - |  |  |
| 6 | `Balance` | Balance | Num | 19.6 | - |  |  |
| 7 | `FrnBlnc` | Balance (FC) | Num | 19.6 | - |  |  |
| 8 | `Valid` | Confirmed | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 9 | `RevalRate` | Revaluation Rate | Num | 19.6 | - |  |  |
| 10 | `Delta` | Difference in LC | Num | 19.6 | - |  |  |
| 11 | `FCCurrency` | Foreign Currency | nVarChar | 3 | - |  |  |
| 12 | `JdtAcctCod` | Journal Account Code | nVarChar | 15 | - |  |  |
| 13 | `BaseRef` | Base Reference | nVarChar | 11 | - |  |  |
| 14 | `JdtType` | Journal Entry Type | VarChar | 1 | - | U | `P` = Primary<br>`G` = Generated<br>`W` = Without Primary<br>`U` = Undefined Type |
| 15 | `RefDate` | Posting Date | Date | 8 | - |  |  |
| 16 | `DueDate` | Due Date | Date | 8 | - |  |  |
| 17 | `TaxDate` | Document Date | Date | 8 | - |  |  |
| 18 | `BPLId` | Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 19 | `CntBlnc` | Converted Balance | Num | 19.6 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | LineNum, TransId, JdtLine, IsSysCurr |
| SYS_CURR | No | IsSysCurr |
