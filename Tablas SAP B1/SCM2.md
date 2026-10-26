# SCM2 - Special Ledger - Analytical Accounting Configuration Rule Goals: Material

- **Tabla:** SCM2
- **Descripción:** Special Ledger - Analytical Accounting Configuration Rule Goals: Material
- **Cantidad de campos:** 22
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SCM2.html

## Campos (22)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `RuleID` | Rule Identification Number | Int | 6 | [OSCM](OSCM.md) |  |  |
| 2 | `GoalNum` | Rule Goal Number | nVarChar | 6 | - |  |  |
| 3 | `TransTpVal` | Transaction Type Number | Int | 6 | - |  |  |
| 4 | `TransTpFld` | Transaction Type Table Field | nVarChar | 20 | - |  |  |
| 5 | `PrfCntVal` | Distribution Rule Code | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 6 | `PrfCntFld` | Distribution Rule Table Field | nVarChar | 20 | - |  |  |
| 7 | `DebitAct` | Debit Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 8 | `CreditAct` | Credit Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 9 | `RevSides` | Revert Debit/Credit Sides | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 10 | `SrcTable` | Main Source Table | nVarChar | 10 | - |  |  |
| 11 | `SrcField` | Main Source Table Field | nVarChar | 20 | - |  |  |
| 12 | `SrcFieldFC` | Source Field, Foreign Currency | nVarChar | 20 | - |  |  |
| 13 | `SrcFieldSC` | Source Field, System Currency | nVarChar | 20 | - |  |  |
| 14 | `Calc` | Calculation Expression | nVarChar | 200 | - |  |  |
| 15 | `CalcFC` | Expression for Foreign Calculation | nVarChar | 200 | - |  |  |
| 16 | `CalcSC` | Expression for System Calculation | nVarChar | 200 | - |  |  |
| 17 | `CalcCond` | Calculation Condition | nVarChar | 200 | - |  |  |
| 18 | `CalcCondFC` | Condition for Foreign Calculation | nVarChar | 200 | - |  |  |
| 19 | `CalcCondSC` | Condition for System Calculation | nVarChar | 200 | - |  |  |
| 20 | `CurrFld` | Table Field with Currency | nVarChar | 20 | - |  |  |
| 21 | `CallProc` | Recalculation Stored Procedure Name | nVarChar | 50 | - |  |  |
| 22 | `ExtCond` | Extended Special Data | nVarChar | 200 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | RuleID, GoalNum |
