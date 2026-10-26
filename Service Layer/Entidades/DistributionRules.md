# DistributionRules — Normas de reparto

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `DistributionRules`
- **Descripción (ES):** Normas de reparto
- **Entity type:** `DistributionRule` (open type: accepts dynamic/UDF properties)
- **Key:** `FactorCode` (Edm.String)
- **DB tables (main / lines):** [OOCR](../../Tablas%20SAP%20B1/OOCR.md), [OCR1](../../Tablas%20SAP%20B1/OCR1.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 8 · **Navigation properties:** 7 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/DistributionRules?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/DistributionRules/$count` | Contar |
| Get by key | `GET /b1s/v2/DistributionRules('value')` | Obtener por clave |
| Create | `POST /b1s/v2/DistributionRules` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/DistributionRules('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/DistributionRules('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/DistributionRules('value')` (only if the B1 object allows removal) | Borrar |

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `FactorCode` 🔑 | Edm.String | No | Factor Code | Código de factor |
| 2 | `FactorDescription` | Edm.String | Yes | Factor Description | Descripción del factor |
| 3 | `TotalFactor` | Edm.Double | Yes | Total Factor | Factor total |
| 4 | `Direct` | Edm.String | Yes | Direct | Directo |
| 5 | `InWhichDimension` | Edm.Int32 | Yes | In Which Dimension | En qué dimensión |
| 6 | `Active` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Active | Activo |
| 7 | `IsFixedAmount` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Fixed Amount | Es importe fijo |
| 8 | `DistributionRuleLines` | Collection([DistributionRuleLine](../Tipos-Complejos/DistributionRuleLine.md)) | Yes | Distribution Rule Lines | Líneas de la norma de reparto |

## Navigation properties (7)

Use `GET /b1s/v2/DistributionRules('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `ProductTrees` | Collection([ProductTree](../Entidades/ProductTrees.md)) | [ProductTrees](ProductTrees.md) |  | Listas de materiales (árbol de producto) |
| `Dimension` | [Dimension](../Entidades/Dimensions.md) | [Dimensions](Dimensions.md) | InWhichDimension → DimensionCode | Dimensión |
| `AdditionalExpenses` | Collection([AdditionalExpense](../Entidades/AdditionalExpenses.md)) | [AdditionalExpenses](AdditionalExpenses.md) |  | Gastos adicionales (fletes) |
| `ChartOfAccounts` | Collection([ChartOfAccount](../Entidades/ChartOfAccounts.md)) | [ChartOfAccounts](ChartOfAccounts.md) |  | Plan de cuentas (cuentas de mayor) |
| `ProductionOrders` | Collection([ProductionOrder](../Entidades/ProductionOrders.md)) | [ProductionOrders](ProductionOrders.md) |  | Órdenes de fabricación |
| `BudgetScenarios` | Collection([BudgetScenario](../Entidades/BudgetScenarios.md)) | [BudgetScenarios](BudgetScenarios.md) |  | Escenarios de presupuesto |
| `Deposits` | Collection([Deposit](../Entidades/Deposits.md)) | [Deposits](Deposits.md) |  | Depósitos |
