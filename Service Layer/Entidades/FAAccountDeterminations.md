# FAAccountDeterminations — Determinación de cuentas de activos fijos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `FAAccountDeterminations`
- **Descripción (ES):** Determinación de cuentas de activos fijos
- **Entity type:** `FAAccountDetermination`
- **Key:** `Code` (Edm.String)
- **DB tables (main / lines):** [OADT](../../Tablas%20SAP%20B1/OADT.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 21 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/FAAccountDeterminations?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/FAAccountDeterminations/$count` | Contar |
| Get by key | `GET /b1s/v2/FAAccountDeterminations('value')` | Obtener por clave |
| Create | `POST /b1s/v2/FAAccountDeterminations` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/FAAccountDeterminations('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/FAAccountDeterminations('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/FAAccountDeterminations('value')` (only if the B1 object allows removal) | Borrar |

## Properties (21)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.String | No | Code | Código |
| 2 | `Description` | Edm.String | Yes | Description | Descripción |
| 3 | `AssetBalanceSheetAccount` | Edm.String | Yes | Asset Balance Sheet Account | Cuenta de balance del activo |
| 4 | `ClearingAccountAcquisition` | Edm.String | Yes | Clearing Account Acquisition | Cuenta puente de adquisición |
| 5 | `RevaluationReserveAccount` | Edm.String | Yes | Revaluation Reserve Account | Cuenta de reserva por revalorización |
| 6 | `RevaluationReserveClearing` | Edm.String | Yes | Revaluation Reserve Clearing | Compensación de reserva por revalorización |
| 7 | `OrdinaryDepreciation` | Edm.String | Yes | Ordinary Depreciation | Amortización ordinaria |
| 8 | `AccumulatedOrdinaryDepr` | Edm.String | Yes | Accumulated Ordinary Depr | Amortización ordinaria acumulada |
| 9 | `UnplannedDepreciation` | Edm.String | Yes | Unplanned Depreciation | Amortización no planificada |
| 10 | `AccumulatedUnplannedDepr` | Edm.String | Yes | Accumulated Unplanned Depr | Amortización no planificada acumulada |
| 11 | `SpecialDepreciation` | Edm.String | Yes | Special Depreciation | Amortización especial |
| 12 | `AccumulatedSpecialDepr` | Edm.String | Yes | Accumulated Special Depr | Amortización especial acumulada |
| 13 | `RevenuefromAssetSalesNet` | Edm.String | Yes | Revenuefrom Asset Sales Net | Ingreso neto por venta de activos |
| 14 | `RetirementwithExpenseNet` | Edm.String | Yes | Retirementwith Expense Net | Baja con gasto (neto) |
| 15 | `RetirementwithRevenueNet` | Edm.String | Yes | Retirementwith Revenue Net | Baja con ingreso (neto) |
| 16 | `LeavewithExpenseNBVGross` | Edm.String | Yes | Leavewith Expense NBV Gross | Baja con gasto (valor neto contable bruto) |
| 17 | `LeavewithRevenueNBVGross` | Edm.String | Yes | Leavewith Revenue NBV Gross | Baja con ingreso (valor neto contable bruto) |
| 18 | `RevenueAccountforRetirement` | Edm.String | Yes | Revenue Accountfor Retirement | Cuenta de ingresos por baja |
| 19 | `RevenueClearingAccount` | Edm.String | Yes | Revenue Clearing Account | Cuenta de compensación de ingresos |
| 20 | `RevaluationAccount` | Edm.String | Yes | Revaluation Account | Cuenta de revalorización |
| 21 | `RevaluationLossAcct` | Edm.String | Yes | Revaluation Loss Account | Cuenta de pérdida por revalorización |

## Navigation properties (1)

Use `GET /b1s/v2/FAAccountDeterminations('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `ChartOfAccount` | [ChartOfAccount](../Entidades/ChartOfAccounts.md) | [ChartOfAccounts](ChartOfAccounts.md) | AssetBalanceSheetAccount → Code | Plan de cuentas (cuentas de mayor) |
