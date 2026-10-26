# ODUT - Dunning Terms

- **Tabla:** ODUT
- **Descripción:** Dunning Terms
- **Cantidad de campos:** 20
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ODUT.html

## Campos (20)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `TermCode` | Dunning Term Code | nVarChar | 25 | - |  |  |
| 2 | `TermName` | Dunning Term Name | nVarChar | 100 | - |  |  |
| 3 | `GrpMethod` | Grouping Method | VarChar | 1 | - | B | `I` = One Letter per Invoice<br>`L` = One Letter per Dunning Level<br>`B` = One Letter per BP |
| 4 | `YearDays` | Days in Year | Int | 6 | - | 360 |  |
| 5 | `MonthDays` | Days in Month | Int | 6 | - | 30 |  |
| 6 | `RemIntrst` | Calc. Interest Rem/Orig Sum | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 7 | `XchgOrig` | Exchange Rate Orig/Current | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 8 | `YearlyRate` | Yearly Interest Rate | Num | 19.6 | - |  |  |
| 9 | `MaxLevel` | Max Dunning Level | Int | 6 | - | 0 |  |
| 10 | `TotalFee` | All Total Fee | Num | 19.6 | - |  |  |
| 11 | `FeeCurr` | All Fee Currency | nVarChar | 3 | - |  |  |
| 12 | `MinBalance` | All Min. Balance | Num | 19.6 | - |  |  |
| 13 | `BalCurr` | All Balance Currency | nVarChar | 3 | - |  |  |
| 14 | `CalcIntr` | All Calc. Interest | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 15 | `LetterFrmt` | All Letter Format | nVarChar | 8 | - |  |  |
| 16 | `HiLtrFrmt` | Apply Highest Letter Template | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 17 | `DateCalInt` | Base Date for Interest Calc. | VarChar | 1 | - | Y | `Y` = From Due Date<br>`N` = From Last Dunning Run |
| 18 | `AutoPost` | Automatic Posting | VarChar | 1 | - | N | `N` = No<br>`B` = Interest and Fee<br>`I` = Interest Only<br>`F` = Fee Only |
| 19 | `IntrAcc` | Interest Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 20 | `FeeAcc` | Fee Account | nVarChar | 15 | [OACT](OACT.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TermCode |
