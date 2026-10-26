# AssetDepreciationGroups — Grupos de amortización de activos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `AssetDepreciationGroups`
- **Descripción (ES):** Grupos de amortización de activos
- **Entity type:** `AssetDepreciationGroup`
- **Key:** `Code` (Edm.String)
- **DB tables (main / lines):** [OADG](../../Tablas%20SAP%20B1/OADG.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 3 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/AssetDepreciationGroups?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/AssetDepreciationGroups/$count` | Contar |
| Get by key | `GET /b1s/v2/AssetDepreciationGroups('value')` | Obtener por clave |
| Create | `POST /b1s/v2/AssetDepreciationGroups` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/AssetDepreciationGroups('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/AssetDepreciationGroups('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/AssetDepreciationGroups('value')` (only if the B1 object allows removal) | Borrar |

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.String | No | Code | Código |
| 2 | `Description` | Edm.String | Yes | Description | Descripción |
| 3 | `Group` | Edm.String | Yes | Group | Grupo |

## Navigation properties (1)

Use `GET /b1s/v2/AssetDepreciationGroups('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Items` | Collection([Item](../Entidades/Items.md)) | [Items](Items.md) |  | Artículos |
