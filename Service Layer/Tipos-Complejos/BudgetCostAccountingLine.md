# BudgetCostAccountingLine — Líneas de contabilidad de costos del presupuesto

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `BudgetCostAccountingLine`
- **Descripción (ES):** Líneas de contabilidad de costos del presupuesto
- **Description (EN):** Budget Cost Accounting Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 6

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DistrRuleCode` | Edm.String | Yes | Distr Rule Code | Código de norma de reparto |
| 2 | `Dimension` | Edm.Int32 | Yes | Dimension | Dimensión |
| 3 | `DistrRuleDebitLC` | Edm.Double | Yes | Distr Rule Debit LC (local currency) | Debe de norma de reparto (moneda local) |
| 4 | `DistrRuleDebitSC` | Edm.Double | Yes | Distr Rule Debit SC (system currency) | Debe de norma de reparto (moneda del sistema) |
| 5 | `DistrRuleCreditLC` | Edm.Double | Yes | Distr Rule Credit LC (local currency) | Haber de norma de reparto (moneda local) |
| 6 | `DistrRuleCreditSC` | Edm.Double | Yes | Distr Rule Credit SC (system currency) | Haber de norma de reparto (moneda del sistema) |

## Used by (properties)

- [Budget](../Entidades/Budgets.md).`BudgetCostAccountingLines`
