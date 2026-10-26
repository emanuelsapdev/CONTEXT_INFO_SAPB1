# PMG8 - Project Management - Summary

- **Tabla:** PMG8
- **Descripción:** Project Management - Summary
- **Cantidad de campos:** 37
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PMG8.html

## Campos (37)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | - |  |  |
| 2 | `LineID` | Row No. | Int | 11 | - |  |  |
| 3 | `PhBudget` | Subproject Budget | Num | 19.6 | - |  |  |
| 4 | `OpenAmtAP` | Open Amount (A/P) | Num | 19.6 | - |  |  |
| 5 | `InvoicedAP` | Invoiced (A/P) | Num | 19.6 | - |  |  |
| 6 | `TotalAP` | Total (A/P) | Num | 19.6 | - |  |  |
| 7 | `TotVarAP` | Total Variance (A/P) | Num | 19.6 | - |  |  |
| 8 | `VarPercAP` | Variance Percentage (A/P) | Num | 19.6 | - |  |  |
| 9 | `AccPhBudg` | Accumulated Subproject Budget | Num | 19.6 | - |  |  |
| 10 | `AccOpAmAP` | Accumulated Open Amount (A/P) | Num | 19.6 | - |  |  |
| 11 | `AccInvAP` | Accumulated Invoiced (A/P) | Num | 19.6 | - |  |  |
| 12 | `AccTotAP` | Accumulated Total (A/P) | Num | 19.6 | - |  |  |
| 13 | `AccTVarAP` | Accumulated Total Variance (A/P) | Num | 19.6 | - |  |  |
| 14 | `AccVPercAP` | Accumulated Variance Percentage (A/P) | Num | 19.6 | - |  |  |
| 15 | `PoPhAmt` | Potential Subproject Amount | Num | 19.6 | - |  |  |
| 16 | `OpenAmtAR` | Open Amount (A/R) | Num | 19.6 | - |  |  |
| 17 | `InvoicedAR` | Invoiced (A/R) | Num | 19.6 | - |  |  |
| 18 | `TotalAR` | Total (A/R) | Num | 19.6 | - |  |  |
| 19 | `TotVarAR` | Total Variance (A/R) | Num | 19.6 | - |  |  |
| 20 | `VarPercAR` | Variance Percentage (A/R) | Num | 19.6 | - |  |  |
| 21 | `AccPoPhAmt` | Accumulated Potential Subproject Amount | Num | 19.6 | - |  |  |
| 22 | `AccOpAmAR` | Accumulated Open Amount (A/R) | Num | 19.6 | - |  |  |
| 23 | `AccInvAR` | Accumulated Invoiced (A/R) | Num | 19.6 | - |  |  |
| 24 | `AccTotAR` | Accumulated Total (A/R) | Num | 19.6 | - |  |  |
| 25 | `AccTVarAR` | Accumulated Total Variance (A/R) | Num | 19.6 | - |  |  |
| 26 | `AccVPercAR` | Accumulated Variance Percentage (A/R) | Num | 19.6 | - |  |  |
| 27 | `ActICCost` | Actual Item Component Cost | Num | 19.6 | - |  |  |
| 28 | `ActRCCost` | Actual Resource Component Cost | Num | 19.6 | - |  |  |
| 29 | `ActAddCost` | Actual Additional Cost | Num | 19.6 | - |  |  |
| 30 | `ActPrCost` | Actual Product Cost | Num | 19.6 | - |  |  |
| 31 | `ActBPrCost` | Actual By-Product Cost | Num | 19.6 | - |  |  |
| 32 | `TotalVar` | Total Variance | Num | 19.6 | - |  |  |
| 33 | `DueDate` | Due Date | Date | 8 | - |  |  |
| 34 | `CloseDate` | Actual Closing Date | Date | 8 | - |  |  |
| 35 | `Overdue` | Overdue | Int | 11 | - | 0 |  |
| 36 | `Valid` | If the calculated data is valid | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 37 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineID |
