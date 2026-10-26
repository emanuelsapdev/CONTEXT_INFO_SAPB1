# SCM3 - Special Ledger - Analytical Accounting Configuration Rule Additional Calculations: Material

- **Tabla:** SCM3
- **Descripción:** Special Ledger - Analytical Accounting Configuration Rule Additional Calculations: Material
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SCM3.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `RuleID` | Rule Identification Number | Int | 6 | [OSCM](OSCM.md) |  |  |
| 2 | `FldNum` | Result Field Number | Int | 6 | - |  |  |
| 3 | `SrcTable` | Main Source Table | nVarChar | 20 | - |  |  |
| 4 | `SrcField` | Main Source Table Field | nVarChar | 20 | - |  |  |
| 5 | `CalcCase` | Additional Calcul. Expression | nVarChar | 200 | - |  |  |
| 6 | `CalcTable` | Main Calculation Expression | nVarChar | 200 | - |  |  |
| 7 | `CondCase` | Additional Calcul. Condition | nVarChar | 200 | - |  |  |
| 8 | `CondTable` | Main Calculation Condition | nVarChar | 200 | - |  |  |
| 9 | `Grouping` | Group by Clause | nVarChar | 100 | - |  |  |
| 10 | `CallProc` | Recalculation Stored Procedure Name | nVarChar | 50 | - |  |  |
| 11 | `ExtCond` | Extended Special Data | nVarChar | 200 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | RuleID, FldNum |
