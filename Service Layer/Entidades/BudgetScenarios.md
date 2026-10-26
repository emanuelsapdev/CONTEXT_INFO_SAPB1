# BudgetScenarios — Escenarios de presupuesto

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `BudgetScenarios`
- **Descripción (ES):** Escenarios de presupuesto
- **Entity type:** `BudgetScenario` (open type: accepts dynamic/UDF properties)
- **Key:** `Numerator` (Edm.Int32)
- **DB tables (main / lines):** [OBGS](../../Tablas%20SAP%20B1/OBGS.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 12 · **Navigation properties:** 3 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/BudgetScenarios?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/BudgetScenarios/$count` | Contar |
| Get by key | `GET /b1s/v2/BudgetScenarios(1)` | Obtener por clave |
| Create | `POST /b1s/v2/BudgetScenarios` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/BudgetScenarios(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/BudgetScenarios(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/BudgetScenarios(1)` (only if the B1 object allows removal) | Borrar |

## Properties (12)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Name` | Edm.String | Yes | Name | Nombre |
| 2 | `InitialRatioPercentage` | Edm.Double | Yes | Initial Ratio Percentage | Porcentaje de proporción inicial |
| 3 | `StartofFiscalYear` | Edm.DateTimeOffset | Yes | Startof Fiscal Year | Inicio del ejercicio |
| 4 | `BasicBudget` | Edm.Int32 | Yes | Basic Budget | Presupuesto básico |
| 5 | `Numerator` 🔑 | Edm.Int32 | No | Numerator | Numerador |
| 6 | `RoundingMethod` | [BoRoundingMethod](../Enums/BoRoundingMethod.md) | Yes | Rounding Method | Método de redondeo |
| 7 | `Project` | Edm.String | Yes | Project | Proyecto |
| 8 | `DistributionRule` | Edm.String | Yes | Distribution Rule | Norma de reparto |
| 9 | `DistributionRule2` | Edm.String | Yes | Distribution Rule 2 | Norma de reparto 2 |
| 10 | `DistributionRule3` | Edm.String | Yes | Distribution Rule 3 | Norma de reparto 3 |
| 11 | `DistributionRule4` | Edm.String | Yes | Distribution Rule 4 | Norma de reparto 4 |
| 12 | `DistributionRule5` | Edm.String | Yes | Distribution Rule 5 | Norma de reparto 5 |

## Navigation properties (3)

Use `GET /b1s/v2/BudgetScenarios(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Budgets` | Collection([Budget](../Entidades/Budgets.md)) | [Budgets](Budgets.md) |  | Presupuestos |
| `Project2` | [Project](../Entidades/Projects.md) | [Projects](Projects.md) | Project → Code | Proyectos |
| `DistributionRule6` | [DistributionRule](../Entidades/DistributionRules.md) | [DistributionRules](DistributionRules.md) | DistributionRule → FactorCode | Normas de reparto |
