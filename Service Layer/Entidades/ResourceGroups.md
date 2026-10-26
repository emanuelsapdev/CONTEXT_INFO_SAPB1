# ResourceGroups — Grupos de recursos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ResourceGroups`
- **Descripción (ES):** Grupos de recursos
- **Entity type:** `ResourceGroup`
- **Key:** `Code` (Edm.Int32)
- **DB tables (main / lines):** [ORSB](../../Tablas%20SAP%20B1/ORSB.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 24 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ResourceGroups?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ResourceGroups/$count` | Contar |
| Get by key | `GET /b1s/v2/ResourceGroups(1)` | Obtener por clave |
| Create | `POST /b1s/v2/ResourceGroups` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ResourceGroups(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ResourceGroups(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/ResourceGroups(1)` (only if the B1 object allows removal) | Borrar |

## Properties (24)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.Int32 | No | Code | Código |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `Type` | [ResourceTypeEnum](../Enums/ResourceTypeEnum.md) | Yes | Type | Tipo |
| 4 | `CostName1` | Edm.String | Yes | Cost Name 1 | Nombre de costo 1 |
| 5 | `Cost1` | Edm.Double | Yes | Cost 1 | Costo 1 |
| 6 | `CostName2` | Edm.String | Yes | Cost Name 2 | Nombre de costo 2 |
| 7 | `Cost2` | Edm.Double | Yes | Cost 2 | Costo 2 |
| 8 | `CostName3` | Edm.String | Yes | Cost Name 3 | Nombre de costo 3 |
| 9 | `Cost3` | Edm.Double | Yes | Cost 3 | Costo 3 |
| 10 | `CostName4` | Edm.String | Yes | Cost Name 4 | Nombre de costo 4 |
| 11 | `Cost4` | Edm.Double | Yes | Cost 4 | Costo 4 |
| 12 | `CostName5` | Edm.String | Yes | Cost Name 5 | Nombre de costo 5 |
| 13 | `Cost5` | Edm.Double | Yes | Cost 5 | Costo 5 |
| 14 | `CostName6` | Edm.String | Yes | Cost Name 6 | Nombre de costo 6 |
| 15 | `Cost6` | Edm.Double | Yes | Cost 6 | Costo 6 |
| 16 | `CostName7` | Edm.String | Yes | Cost Name 7 | Nombre de costo 7 |
| 17 | `Cost7` | Edm.Double | Yes | Cost 7 | Costo 7 |
| 18 | `CostName8` | Edm.String | Yes | Cost Name 8 | Nombre de costo 8 |
| 19 | `Cost8` | Edm.Double | Yes | Cost 8 | Costo 8 |
| 20 | `CostName9` | Edm.String | Yes | Cost Name 9 | Nombre de costo 9 |
| 21 | `Cost9` | Edm.Double | Yes | Cost 9 | Costo 9 |
| 22 | `CostName10` | Edm.String | Yes | Cost Name 10 | Nombre de costo 10 |
| 23 | `Cost10` | Edm.Double | Yes | Cost 10 | Costo 10 |
| 24 | `NumOfUnitsText` | Edm.String | Yes | Number Of Units Text | Texto de cantidad de unidades |

## Navigation properties (1)

Use `GET /b1s/v2/ResourceGroups(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Resources` | Collection([Resource](../Entidades/Resources.md)) | [Resources](Resources.md) |  | Recursos |
