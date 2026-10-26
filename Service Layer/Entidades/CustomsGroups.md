# CustomsGroups — Grupos aduaneros

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `CustomsGroups`
- **Descripción (ES):** Grupos aduaneros
- **Entity type:** `CustomsGroup` (open type: accepts dynamic/UDF properties)
- **Key:** `Code` (Edm.Int32)
- **DB tables (main / lines):** [OARG](../../Tablas%20SAP%20B1/OARG.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 12 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/CustomsGroups?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/CustomsGroups/$count` | Contar |
| Get by key | `GET /b1s/v2/CustomsGroups(1)` | Obtener por clave |
| Create | `POST /b1s/v2/CustomsGroups` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/CustomsGroups(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/CustomsGroups(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/CustomsGroups(1)` (only if the B1 object allows removal) | Borrar |

## Properties (12)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.Int32 | No | Code | Código |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `Number` | Edm.String | Yes | Number | Número |
| 4 | `Customs` | Edm.Double | Yes | Customs | Aduana |
| 5 | `Purchase` | Edm.Double | Yes | Purchase | Compra |
| 6 | `Other` | Edm.Double | Yes | Other | Otro |
| 7 | `Total` | Edm.Double | Yes | Total | Total |
| 8 | `Locked` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Locked | Bloqueado |
| 9 | `CustomsAllocationAccount` | Edm.String | Yes | Customs Allocation Account | Cuenta de asignación de aduana |
| 10 | `CustomsExpenseAccount` | Edm.String | Yes | Customs Expense Account | Cuenta de gastos de aduana |
| 11 | `PortAddress` | Edm.String | Yes | Port Address | Dirección del puerto |
| 12 | `PortState` | Edm.String | Yes | Port State | Estado del puerto |

## Navigation properties (2)

Use `GET /b1s/v2/CustomsGroups(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Items` | Collection([Item](../Entidades/Items.md)) | [Items](Items.md) |  | Artículos |
| `ChartOfAccount` | [ChartOfAccount](../Entidades/ChartOfAccounts.md) | [ChartOfAccounts](ChartOfAccounts.md) | CustomsAllocationAccount → Code | Plan de cuentas (cuentas de mayor) |
