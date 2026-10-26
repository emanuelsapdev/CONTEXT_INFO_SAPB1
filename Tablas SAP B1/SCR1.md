# SCR1 - Special Ledger - Analytical Accounting Configuration Rule Conditions: Revenues & Expenses

- **Tabla:** SCR1
- **Descripción:** Special Ledger - Analytical Accounting Configuration Rule Conditions: Revenues & Expenses
- **Cantidad de campos:** 15
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SCR1.html

## Campos (15)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `RuleID` | Rule Identification Number | Int | 6 | [OSCR](OSCR.md) |  |  |
| 2 | `CondNum` | Condition Number | Int | 6 | - |  |  |
| 3 | `Value1` | Static Value | nVarChar | 200 | - |  |  |
| 4 | `Table1` | Table Name | nVarChar | 20 | - |  |  |
| 5 | `Field1` | Table Field Name | nVarChar | 200 | - |  |  |
| 6 | `Cond1` | Value Selection Condition | nVarChar | 200 | - |  |  |
| 7 | `Group1` | Group by Clause | nVarChar | 100 | - |  |  |
| 8 | `Relation` | Comparison Operator | nVarChar | 50 | - |  |  |
| 9 | `Value2` | Static Value | nVarChar | 200 | - |  |  |
| 10 | `Table2` | Table Name | nVarChar | 20 | - |  |  |
| 11 | `Field2` | Table Field Name | nVarChar | 200 | - |  |  |
| 12 | `Cond2` | Comparison Operator | nVarChar | 200 | - |  |  |
| 13 | `Group2` | Group by Clause | nVarChar | 100 | - |  |  |
| 14 | `ExtCond1` | Extended Special Data | nVarChar | 200 | - |  |  |
| 15 | `ExtCond2` | Extended Special Data | nVarChar | 200 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | RuleID, CondNum |
