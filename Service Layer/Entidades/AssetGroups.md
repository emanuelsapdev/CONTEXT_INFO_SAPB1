# AssetGroups — Grupos de activos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `AssetGroups`
- **Descripción (ES):** Grupos de activos
- **Entity type:** `AssetGroup`
- **Key:** `Code` (Edm.String)
- **DB tables (main / lines):** [OAGS](../../Tablas%20SAP%20B1/OAGS.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 2 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/AssetGroups?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/AssetGroups/$count` | Contar |
| Get by key | `GET /b1s/v2/AssetGroups('value')` | Obtener por clave |
| Create | `POST /b1s/v2/AssetGroups` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/AssetGroups('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/AssetGroups('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/AssetGroups('value')` (only if the B1 object allows removal) | Borrar |

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.String | No | Code | Código |
| 2 | `Description` | Edm.String | Yes | Description | Descripción |

## Navigation properties (1)

Use `GET /b1s/v2/AssetGroups('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Items` | Collection([Item](../Entidades/Items.md)) | [Items](Items.md) |  | Artículos |
