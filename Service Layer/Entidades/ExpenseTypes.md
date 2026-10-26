# ExpenseTypes — Tipos de gastos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ExpenseTypes`
- **Descripción (ES):** Tipos de gastos
- **Entity type:** `ExpenseTypeData`
- **Key:** `ExpenseType` (Edm.String)
- **DB tables (main / lines):** [OEXT](../../Tablas%20SAP%20B1/OEXT.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 5 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ExpenseTypes?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ExpenseTypes/$count` | Contar |
| Get by key | `GET /b1s/v2/ExpenseTypes('value')` | Obtener por clave |
| Create | `POST /b1s/v2/ExpenseTypes` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ExpenseTypes('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ExpenseTypes('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/ExpenseTypes('value')` (only if the B1 object allows removal) | Borrar |

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ExpenseType` 🔑 | Edm.String | No | Expense Type | Tipo de gasto |
| 2 | `ExpenseName` | Edm.String | Yes | Expense Name | Nombre del gasto |
| 3 | `ExpenseAccount` | Edm.String | Yes | Expense Account | Cuenta de gastos |
| 4 | `PaidByCompany` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Paid By Company | Pagado por la sociedad |
| 5 | `VatGroup` | Edm.String | Yes | Vat Group | Grupo de IVA (indicador de impuesto) |

## Navigation properties (2)

Use `GET /b1s/v2/ExpenseTypes('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `ChartOfAccount` | [ChartOfAccount](../Entidades/ChartOfAccounts.md) | [ChartOfAccounts](ChartOfAccounts.md) | ExpenseAccount → Code | Plan de cuentas (cuentas de mayor) |
| `SalesTaxCode` | [SalesTaxCode](../Entidades/SalesTaxCodes.md) | [SalesTaxCodes](SalesTaxCodes.md) | VatGroup → Code | Códigos del impuesto sobre ventas |
