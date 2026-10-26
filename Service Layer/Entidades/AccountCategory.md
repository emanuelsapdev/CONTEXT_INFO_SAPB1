# AccountCategory — Categoría de cuenta

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `AccountCategory`
- **Descripción (ES):** Categoría de cuenta
- **Entity type:** `AccountCategory`
- **Key:** `CategoryCode` (Edm.Int32)
- **DB tables (main / lines):** [OACG](../../Tablas%20SAP%20B1/OACG.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 3 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/AccountCategory?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/AccountCategory/$count` | Contar |
| Get by key | `GET /b1s/v2/AccountCategory(1)` | Obtener por clave |
| Create | `POST /b1s/v2/AccountCategory` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/AccountCategory(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/AccountCategory(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/AccountCategory(1)` (only if the B1 object allows removal) | Borrar |

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `CategoryCode` 🔑 | Edm.Int32 | No | Category Code | Código de categoría |
| 2 | `CategoryName` | Edm.String | Yes | Category Name | Nombre de la categoría |
| 3 | `CategorySource` | [AccountCategorySourceEnum](../Enums/AccountCategorySourceEnum.md) | Yes | Category Source | Origen de la categoría |

## Navigation properties (1)

Use `GET /b1s/v2/AccountCategory(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `ChartOfAccounts` | Collection([ChartOfAccount](../Entidades/ChartOfAccounts.md)) | [ChartOfAccounts](ChartOfAccounts.md) |  | Plan de cuentas (cuentas de mayor) |
