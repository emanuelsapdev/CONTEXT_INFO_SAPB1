# Budgets — Presupuestos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `Budgets`
- **Descripción (ES):** Presupuestos
- **Entity type:** `Budget` (open type: accepts dynamic/UDF properties)
- **Key:** `Numerator` (Edm.Int32)
- **DB tables (main / lines):** [OBGT](../../Tablas%20SAP%20B1/OBGT.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 25 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/Budgets?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/Budgets/$count` | Contar |
| Get by key | `GET /b1s/v2/Budgets(1)` | Obtener por clave |
| Create | `POST /b1s/v2/Budgets` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/Budgets(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/Budgets(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/Budgets(1)` (only if the B1 object allows removal) | Borrar |

## Properties (25)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `FutureAnnualExpensesCreditSys` | Edm.Double | Yes | Future Annual Expenses Credit (system currency) | Haber de gastos anuales futuros (moneda del sistema) |
| 2 | `FutureAnnualExpensesCreditLoc` | Edm.Double | Yes | Future Annual Expenses Credit Loc | Haber de gastos anuales futuros (moneda local) |
| 3 | `FutureAnnualExpensesDebitSys` | Edm.Double | Yes | Future Annual Expenses Debit (system currency) | Debe de gastos anuales futuros (moneda del sistema) |
| 4 | `FutureAnnualExpensesDebitLoc` | Edm.Double | Yes | Future Annual Expenses Debit Loc | Debe de gastos anuales futuros (moneda local) |
| 5 | `FutureAnnualRevenuesCredit` | Edm.Double | Yes | Future Annual Revenues Credit | Haber de ingresos anuales futuros |
| 6 | `FutureAnnualRevenuesDebit` | Edm.Double | Yes | Future Annual Revenues Debit | Debe de ingresos anuales futuros |
| 7 | `FutureRevenuesDebitSys` | Edm.Double | Yes | Future Revenues Debit (system currency) | Debe de ingresos futuros (moneda del sistema) |
| 8 | `FutureRevenuesDebitLoc` | Edm.Double | Yes | Future Revenues Debit Loc | Debe de ingresos futuros (moneda local) |
| 9 | `ParentAccPercent` | Edm.Double | Yes | Parent Account Percent | Porcentaje de la cuenta padre |
| 10 | `StartofFiscalYear` | Edm.DateTimeOffset | Yes | Startof Fiscal Year | Inicio del ejercicio |
| 11 | `ParentAccountKey` | Edm.String | Yes | Parent Account Key | Clave de cuenta padre |
| 12 | `TotalAnnualBudgetDebitSys` | Edm.Double | Yes | Total Annual Budget Debit (system currency) | Presupuesto anual total debe (moneda del sistema) |
| 13 | `BudgetBalanceDebitSys` | Edm.Double | Yes | Budget Balance Debit (system currency) | Saldo de presupuesto debe (moneda del sistema) |
| 14 | `BudgetBalanceDebitLoc` | Edm.Double | Yes | Budget Balance Debit Loc | Saldo de presupuesto debe (moneda local) |
| 15 | `TotalAnnualBudgetDebitLoc` | Edm.Double | Yes | Total Annual Budget Debit Loc | Presupuesto anual total debe (moneda local) |
| 16 | `TotalAnnualBudgetCreditSys` | Edm.Double | Yes | Total Annual Budget Credit (system currency) | Presupuesto anual total haber (moneda del sistema) |
| 17 | `TotalAnnualBudgetCreditLoc` | Edm.Double | Yes | Total Annual Budget Credit Loc | Presupuesto anual total haber (moneda local) |
| 18 | `BudgetBalanceCreditSys` | Edm.Double | Yes | Budget Balance Credit (system currency) | Saldo de presupuesto haber (moneda del sistema) |
| 19 | `BudgetBalanceCreditLoc` | Edm.Double | Yes | Budget Balance Credit Loc | Saldo de presupuesto haber (moneda local) |
| 20 | `DivisionCode` | Edm.Int32 | Yes | Division Code | Código de división |
| 21 | `AccountCode` | Edm.String | Yes | Account Code | Código de cuenta |
| 22 | `Numerator` 🔑 | Edm.Int32 | No | Numerator | Numerador |
| 23 | `BudgetScenario` | Edm.Int32 | Yes | Budget Scenario | Escenario de presupuesto |
| 24 | `BudgetLines` | Collection([BudgetLine](../Tipos-Complejos/BudgetLine.md)) | Yes | Budget Lines | Líneas del presupuesto |
| 25 | `BudgetCostAccountingLines` | Collection([BudgetCostAccountingLine](../Tipos-Complejos/BudgetCostAccountingLine.md)) | Yes | Budget Cost Accounting Lines | Líneas de contabilidad de costos del presupuesto |

## Navigation properties (2)

Use `GET /b1s/v2/Budgets(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `BudgetDistribution` | [BudgetDistribution](../Entidades/BudgetDistributions.md) | [BudgetDistributions](BudgetDistributions.md) | DivisionCode → DivisionCode | Métodos de distribución del presupuesto |
| `BudgetScenario2` | [BudgetScenario](../Entidades/BudgetScenarios.md) | [BudgetScenarios](BudgetScenarios.md) | BudgetScenario → Numerator | Escenarios de presupuesto |
