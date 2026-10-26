# WebClientDashboards — Cliente web - Dashboards

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `WebClientDashboards`
- **Descripción (ES):** Cliente web - Dashboards
- **Entity type:** `WebClientDashboard`
- **Key:** `Guid` (Edm.String)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 5 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/WebClientDashboards?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/WebClientDashboards/$count` | Contar |
| Get by key | `GET /b1s/v2/WebClientDashboards('value')` | Obtener por clave |
| Create | `POST /b1s/v2/WebClientDashboards` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/WebClientDashboards('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/WebClientDashboards('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/WebClientDashboards('value')` (only if the B1 object allows removal) | Borrar |

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Guid` 🔑 | Edm.String | No | Guid | GUID |
| 2 | `UserId` | Edm.Int32 | Yes | User ID | ID de usuario |
| 3 | `Content` | Edm.String | Yes | Content | Contenido |
| 4 | `Sys` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | (system currency) | Sistema |
| 5 | `WebClientDashboardCards` | Collection([WebClientDashboardCard](../Tipos-Complejos/WebClientDashboardCard.md)) | Yes | Web Client Dashboard Cards | Tarjetas del dashboard del cliente web |
