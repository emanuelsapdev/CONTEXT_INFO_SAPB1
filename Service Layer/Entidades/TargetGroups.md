# TargetGroups — Grupos objetivo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `TargetGroups`
- **Descripción (ES):** Grupos objetivo
- **Entity type:** `TargetGroup`
- **Key:** `TargetGroupCode` (Edm.String)
- **DB tables (main / lines):** [OTGG](../../Tablas%20SAP%20B1/OTGG.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 4 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/TargetGroups?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/TargetGroups/$count` | Contar |
| Get by key | `GET /b1s/v2/TargetGroups('value')` | Obtener por clave |
| Create | `POST /b1s/v2/TargetGroups` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/TargetGroups('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/TargetGroups('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/TargetGroups('value')` (only if the B1 object allows removal) | Borrar |

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TargetGroupCode` 🔑 | Edm.String | No | Target Group Code | Código de grupo objetivo |
| 2 | `TargetGroupName` | Edm.String | Yes | Target Group Name | Nombre del grupo objetivo |
| 3 | `TargetGroupType` | [TargetGroupTypeEnum](../Enums/TargetGroupTypeEnum.md) | Yes | Target Group Type | Tipo de grupo objetivo |
| 4 | `TargetGroupsDetails` | Collection([TargetGroupsDetail](../Tipos-Complejos/TargetGroupsDetail.md)) | Yes | Target Groups Details | Detalles de grupos objetivo |

## Navigation properties (1)

Use `GET /b1s/v2/TargetGroups('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Campaigns` | Collection([Campaign](../Entidades/Campaigns.md)) | [Campaigns](Campaigns.md) |  | Campañas |
