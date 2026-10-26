# AccrualTypes — Tipos de periodificación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `AccrualTypes`
- **Descripción (ES):** Tipos de periodificación
- **Entity type:** `AccrualType` (open type: accepts dynamic/UDF properties)
- **Key:** `Code` (Edm.String)
- **DB tables (main / lines):** [OACR](../../Tablas%20SAP%20B1/OACR.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 5 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/AccrualTypes?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/AccrualTypes/$count` | Contar |
| Get by key | `GET /b1s/v2/AccrualTypes('value')` | Obtener por clave |
| Create | `POST /b1s/v2/AccrualTypes` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/AccrualTypes('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/AccrualTypes('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/AccrualTypes('value')` (only if the B1 object allows removal) | Borrar |

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.String | No | Code | Código |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `PostingAccount` | Edm.String | Yes | Posting Account | Cuenta de contabilización |
| 4 | `CalculationAccount` | Edm.String | Yes | Calculation Account | Cuenta de cálculo |
| 5 | `InterimAccount` | Edm.String | Yes | Interim Account | Cuenta transitoria |

## Navigation properties (1)

Use `GET /b1s/v2/AccrualTypes('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `ChartOfAccount` | [ChartOfAccount](../Entidades/ChartOfAccounts.md) | [ChartOfAccounts](ChartOfAccounts.md) | PostingAccount → Code | Plan de cuentas (cuentas de mayor) |
