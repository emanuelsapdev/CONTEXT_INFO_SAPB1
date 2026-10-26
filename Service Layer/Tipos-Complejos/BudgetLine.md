# BudgetLine — Líneas del presupuesto

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `BudgetLine`
- **Descripción (ES):** Líneas del presupuesto
- **Description (EN):** Budget Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 21

## Properties (21)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `PrecentOfAnnualBudgetAmount` | Edm.Double | Yes | Precent Of Annual Budget Amount | Porcentaje del presupuesto anual |
| 2 | `RowDetails` | Edm.String | Yes | Row Details | Detalles de la línea |
| 3 | `RowNumber` | Edm.Int32 | Yes | Row Number | Número de línea |
| 4 | `FutExpenSysDebit` | Edm.Double | Yes | Fut Expen (system currency) Debit | Debe de gastos futuros (moneda del sistema) |
| 5 | `FutExpenDebit` | Edm.Double | Yes | Fut Expen Debit | Debe de gastos futuros |
| 6 | `FutExpenSysCredit` | Edm.Double | Yes | Fut Expen (system currency) Credit | Haber de gastos futuros (moneda del sistema) |
| 7 | `FutExpenCredit` | Edm.Double | Yes | Fut Expen Credit | Haber de gastos futuros |
| 8 | `FutIncomesSysCredit` | Edm.Double | Yes | Fut Incomes (system currency) Credit | Haber de ingresos futuros (moneda del sistema) |
| 9 | `FutIncomesSysDebit` | Edm.Double | Yes | Fut Incomes (system currency) Debit | Debe de ingresos futuros (moneda del sistema) |
| 10 | `FutIncomesCredit` | Edm.Double | Yes | Fut Incomes Credit | Haber de ingresos futuros |
| 11 | `BudgetSysTotDebit` | Edm.Double | Yes | Budget (system currency) Tot Debit | Total debe del presupuesto (moneda del sistema) |
| 12 | `BalSysTotDebit` | Edm.Double | Yes | Bal (system currency) Tot Debit | Saldo total debe (moneda del sistema) |
| 13 | `BalTotDebit` | Edm.Double | Yes | Bal Tot Debit | Saldo total debe |
| 14 | `BudgetTotCredit` | Edm.Double | Yes | Budget Tot Credit | Total haber del presupuesto |
| 15 | `BudgetSysTotCredit` | Edm.Double | Yes | Budget (system currency) Tot Credit | Total haber del presupuesto (moneda del sistema) |
| 16 | `BudgetTotDebit` | Edm.Double | Yes | Budget Tot Debit | Total debe del presupuesto |
| 17 | `BalSysTotCredit` | Edm.Double | Yes | Bal (system currency) Tot Credit | Saldo total haber (moneda del sistema) |
| 18 | `BalTotCredit` | Edm.Double | Yes | Bal Tot Credit | Saldo total haber |
| 19 | `BudgetKey` | Edm.Int32 | Yes | Budget Key | Clave del presupuesto |
| 20 | `AccountCode` | Edm.String | Yes | Account Code | Código de cuenta |
| 21 | `FutureIncomeDeb` | Edm.Double | Yes | Future Income Deb | Debe de ingresos futuros |

## Used by (properties)

- [Budget](../Entidades/Budgets.md).`BudgetLines`
