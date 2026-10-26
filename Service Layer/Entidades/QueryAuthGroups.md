# QueryAuthGroups — Grupos de autorización de consultas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `QueryAuthGroups`
- **Descripción (ES):** Grupos de autorización de consultas
- **Entity type:** `QueryAuthGroup`
- **Key:** `AuthGroupId` (Edm.Int32)
- **DB tables (main / lines):** [OQAG](../../Tablas%20SAP%20B1/OQAG.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 4 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/QueryAuthGroups?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/QueryAuthGroups/$count` | Contar |
| Get by key | `GET /b1s/v2/QueryAuthGroups(1)` | Obtener por clave |
| Create | `POST /b1s/v2/QueryAuthGroups` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/QueryAuthGroups(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/QueryAuthGroups(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/QueryAuthGroups(1)` (only if the B1 object allows removal) | Borrar |

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AuthGroupCode` | Edm.String | Yes | Auth Group Code | Código de grupo de autorización |
| 2 | `AuthGroupDes` | Edm.String | Yes | Auth Group Des | Descripción del grupo de autorización |
| 3 | `AuthGroupId` 🔑 | Edm.Int32 | No | Auth Group ID | ID del grupo de autorización |
| 4 | `CategoryGroupCollection` | Collection([CategoryGroup](../Tipos-Complejos/CategoryGroup.md)) | Yes | Category Group Collection | Colección de grupos de categorías |

## Service operations that use this type

- [`QueryAuthGroupService_GetQueryAuthGroupList`](../Servicios/QueryAuthGroupService.md#queryauthgroupservice_getqueryauthgrouplist)
