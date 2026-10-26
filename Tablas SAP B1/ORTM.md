# ORTM - Rate Differences

- **Tabla:** ORTM
- **Descripción:** Rate Differences
- **Cantidad de campos:** 20
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ORTM.html

## Campos (20)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `LineNum` | Reconciliation Key | Int | 11 | - |  |  |
| 2 | `Rtmdate` | Posting Date | Date | 8 | - |  |  |
| 3 | `AcctCode` | G/L Account/BP Code | nVarChar | 15 | - |  |  |
| 4 | `IsCard` | Card | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `ActCurrncy` | Document Valuation Currency | nVarChar | 3 | - |  |  |
| 6 | `ActRate` | Document Revaluation Rate | Num | 19.6 | - |  |  |
| 7 | `Balance` | Balance | Num | 19.6 | - |  |  |
| 8 | `FrnBlnc` | FC Balance | Num | 19.6 | - |  |  |
| 9 | `TransNum` | Transaction Number | Int | 11 | - | 0 |  |
| 10 | `Valid` | Confirmed | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 11 | `Delta` | Difference in LC | Num | 19.6 | - |  |  |
| 12 | `IsSysCurr` | In System Currency | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 13 | `StornoDate` | Reversal Date | Date | 8 | - |  |  |
| 14 | `RevalRate` | Revaluation Rate | Num | 19.6 | - |  |  |
| 15 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 16 | `BPLId` | Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 17 | `CntBlnc` | Converted Balance | Num | 19.6 | - |  |  |
| 18 | `TransAmtSC` | Transaction Amount Total | Num | 19.6 | - |  |  |
| 19 | `BalDueSC` | Balance Due Total | Num | 19.6 | - |  |  |
| 20 | `SCAdjust` | SC Adjustment | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | LineNum, IsSysCurr |
| SYS_CURR | No | IsSysCurr |
