# BudgetDistributions — Métodos de distribución del presupuesto

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `BudgetDistributions`
- **Descripción (ES):** Métodos de distribución del presupuesto
- **Entity type:** `BudgetDistribution` (open type: accepts dynamic/UDF properties)
- **Key:** `DivisionCode` (Edm.Int32)
- **DB tables (main / lines):** [OBGD](../../Tablas%20SAP%20B1/OBGD.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 15 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/BudgetDistributions?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/BudgetDistributions/$count` | Contar |
| Get by key | `GET /b1s/v2/BudgetDistributions(1)` | Obtener por clave |
| Create | `POST /b1s/v2/BudgetDistributions` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/BudgetDistributions(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/BudgetDistributions(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/BudgetDistributions(1)` (only if the B1 object allows removal) | Borrar |

## Properties (15)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `September` | Edm.Double | Yes | September | Septiembre |
| 2 | `August` | Edm.Double | Yes | August | Agosto |
| 3 | `July` | Edm.Double | Yes | July | Julio |
| 4 | `June` | Edm.Double | Yes | June | Junio |
| 5 | `May` | Edm.Double | Yes | May | Mayo |
| 6 | `April` | Edm.Double | Yes | April | Abril |
| 7 | `March` | Edm.Double | Yes | March | Marzo |
| 8 | `February` | Edm.Double | Yes | February | Febrero |
| 9 | `December` | Edm.Double | Yes | December | Diciembre |
| 10 | `November` | Edm.Double | Yes | November | Noviembre |
| 11 | `October` | Edm.Double | Yes | October | Octubre |
| 12 | `January` | Edm.Double | Yes | January | Enero |
| 13 | `BudgetAmount` | Edm.Double | Yes | Budget Amount | Importe de presupuesto |
| 14 | `Description` | Edm.String | Yes | Description | Descripción |
| 15 | `DivisionCode` 🔑 | Edm.Int32 | No | Division Code | Código de división |

## Navigation properties (1)

Use `GET /b1s/v2/BudgetDistributions(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Budgets` | Collection([Budget](../Entidades/Budgets.md)) | [Budgets](Budgets.md) |  | Presupuestos |
