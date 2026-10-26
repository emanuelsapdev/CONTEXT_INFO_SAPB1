# AdditionalExpenses — Gastos adicionales (fletes)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `AdditionalExpenses`
- **Descripción (ES):** Gastos adicionales (fletes)
- **Entity type:** `AdditionalExpense` (open type: accepts dynamic/UDF properties)
- **Key:** `ExpensCode` (Edm.Int32)
- **DB tables (main / lines):** [OEXD](../../Tablas%20SAP%20B1/OEXD.md)
- **ETag / optimistic concurrency:** Yes (`DataVersion`) — send `If-Match` on PATCH/DELETE/actions

- **Properties:** 28 · **Navigation properties:** 4 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/AdditionalExpenses?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/AdditionalExpenses/$count` | Contar |
| Get by key | `GET /b1s/v2/AdditionalExpenses(1)` | Obtener por clave |
| Create | `POST /b1s/v2/AdditionalExpenses` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/AdditionalExpenses(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/AdditionalExpenses(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/AdditionalExpenses(1)` (only if the B1 object allows removal) | Borrar |

## Properties (28)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Name` | Edm.String | Yes | Name | Nombre |
| 2 | `RevenuesAccount` | Edm.String | Yes | Revenues Account | Cuenta de ingresos |
| 3 | `ExpenseAccount` | Edm.String | Yes | Expense Account | Cuenta de gastos |
| 4 | `TaxLiable` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Tax Liable | Sujeto a impuestos |
| 5 | `FixedAmountRevenues` | Edm.Double | Yes | Fixed Amount Revenues | Importe fijo de ingresos |
| 6 | `FixedAmountExpenses` | Edm.Double | Yes | Fixed Amount Expenses | Importe fijo de gastos |
| 7 | `OutputVATGroup` | Edm.String | Yes | Output VAT Group | Grupo de IVA repercutido |
| 8 | `InputVATGroup` | Edm.String | Yes | Input VAT Group | Grupo de IVA soportado |
| 9 | `DistributionMethod` | [BoAeDistMthd](../Enums/BoAeDistMthd.md) | Yes | Distribution Method | Método de distribución |
| 10 | `Includein1099` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Includein 1099 | Incluir en 1099 |
| 11 | `FreightOffsetAccount` | Edm.String | Yes | Freight Offset Account | Contracuenta de gastos adicionales |
| 12 | `WTLiable` | Edm.String | Yes | Withholding Tax Liable | Sujeto a retención |
| 13 | `ExpensCode` 🔑 | Edm.Int32 | No | Expens Code | Código de gasto |
| 14 | `ExpenseExemptedAccount` | Edm.String | Yes | Expense Exempted Account | Cuenta de gastos exentos |
| 15 | `RevenuesExemptedAccount` | Edm.String | Yes | Revenues Exempted Account | Cuenta de ingresos exentos |
| 16 | `DistributionRule` | Edm.String | Yes | Distribution Rule | Norma de reparto |
| 17 | `DrawingMethod` | [DrawingMethodEnum](../Enums/DrawingMethodEnum.md) | Yes | Drawing Method | Método de utilización |
| 18 | `FreightType` | [FreightTypeEnum](../Enums/FreightTypeEnum.md) | Yes | Freight Type | Tipo de gasto adicional |
| 19 | `Stock` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Stock | Stock |
| 20 | `LastPurchasePrice` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Last Purchase Price | Último precio de compra |
| 21 | `Project` | Edm.String | Yes | Project | Proyecto |
| 22 | `DistributionRule2` | Edm.String | Yes | Distribution Rule 2 | Norma de reparto 2 |
| 23 | `DistributionRule3` | Edm.String | Yes | Distribution Rule 3 | Norma de reparto 3 |
| 24 | `DistributionRule4` | Edm.String | Yes | Distribution Rule 4 | Norma de reparto 4 |
| 25 | `DistributionRule5` | Edm.String | Yes | Distribution Rule 5 | Norma de reparto 5 |
| 26 | `DataVersion` | Edm.Int32 | Yes | Data Version | Versión de datos (control de concurrencia) |
| 27 | `SAFTProductType` | [SAFTProductTypeEnum](../Enums/SAFTProductTypeEnum.md) | Yes | SAFT Product Type | Tipo de producto SAF-T |
| 28 | `SAFTProductTypeEx` | Edm.String | Yes | SAFT Product Type Ex | Tipo de producto SAF-T (ampliado) |

## Navigation properties (4)

Use `GET /b1s/v2/AdditionalExpenses(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `ChartOfAccount` | [ChartOfAccount](../Entidades/ChartOfAccounts.md) | [ChartOfAccounts](ChartOfAccounts.md) | RevenuesAccount → Code | Plan de cuentas (cuentas de mayor) |
| `VatGroup` | [VatGroup](../Entidades/VatGroups.md) | [VatGroups](VatGroups.md) | OutputVATGroup → Code | Grupo de IVA (indicador de impuesto) |
| `DistributionRule6` | [DistributionRule](../Entidades/DistributionRules.md) | [DistributionRules](DistributionRules.md) | DistributionRule → FactorCode | Normas de reparto |
| `Project2` | [Project](../Entidades/Projects.md) | [Projects](Projects.md) | Project → Code | Proyectos |
