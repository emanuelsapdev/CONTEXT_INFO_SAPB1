# UserGroups — Grupos de usuarios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `UserGroups`
- **Descripción (ES):** Grupos de usuarios
- **Entity type:** `UserGroup`
- **Key:** `UserGroupId` (Edm.Int32)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 7 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/UserGroups?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/UserGroups/$count` | Contar |
| Get by key | `GET /b1s/v2/UserGroups(1)` | Obtener por clave |
| Create | `POST /b1s/v2/UserGroups` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/UserGroups(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/UserGroups(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/UserGroups(1)` (only if the B1 object allows removal) | Borrar |

## Properties (7)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `UserGroupId` 🔑 | Edm.Int32 | No | User Group ID | ID del grupo de usuarios |
| 2 | `UserGroupName` | Edm.String | Yes | User Group Name | Nombre del grupo de usuarios |
| 3 | `UserGroupDec` | Edm.String | Yes | User Group Dec | Descripción del grupo de usuarios |
| 4 | `TPLId` | Edm.Int32 | Yes | TPL ID | ID de plantilla de impresión |
| 5 | `StartDate` | Edm.DateTimeOffset | Yes | Start Date | Fecha de inicio |
| 6 | `DueDate` | Edm.DateTimeOffset | Yes | Due Date | Fecha de vencimiento |
| 7 | `UserGroupType` | [UserGroupCategoryEnum](../Enums/UserGroupCategoryEnum.md) | Yes | User Group Type | Tipo de grupo de usuarios |
