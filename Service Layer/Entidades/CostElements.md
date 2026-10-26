# CostElements — Elementos de costo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `CostElements`
- **Descripción (ES):** Elementos de costo
- **Entity type:** `CostElement`
- **Key:** `Code` (Edm.String)
- **DB tables (main / lines):** [OCEM](../../Tablas%20SAP%20B1/OCEM.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 3 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/CostElements?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/CostElements/$count` | Contar |
| Get by key | `GET /b1s/v2/CostElements('value')` | Obtener por clave |
| Create | `POST /b1s/v2/CostElements` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/CostElements('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/CostElements('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/CostElements('value')` (only if the B1 object allows removal) | Borrar |

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.String | No | Code | Código |
| 2 | `Description` | Edm.String | Yes | Description | Descripción |
| 3 | `IsActive` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Active | Está activo |

## Navigation properties (1)

Use `GET /b1s/v2/CostElements('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `ChartOfAccounts` | Collection([ChartOfAccount](../Entidades/ChartOfAccounts.md)) | [ChartOfAccounts](ChartOfAccounts.md) |  | Plan de cuentas (cuentas de mayor) |
