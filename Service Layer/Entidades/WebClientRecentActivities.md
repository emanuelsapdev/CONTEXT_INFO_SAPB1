# WebClientRecentActivities — Cliente web - Actividades recientes

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `WebClientRecentActivities`
- **Descripción (ES):** Cliente web - Actividades recientes
- **Entity type:** `WebClientRecentActivity`
- **Key:** `Guid` (Edm.String)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 10 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/WebClientRecentActivities?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/WebClientRecentActivities/$count` | Contar |
| Get by key | `GET /b1s/v2/WebClientRecentActivities('value')` | Obtener por clave |
| Create | `POST /b1s/v2/WebClientRecentActivities` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/WebClientRecentActivities('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/WebClientRecentActivities('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/WebClientRecentActivities('value')` (only if the B1 object allows removal) | Borrar |

## Properties (10)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Guid` 🔑 | Edm.String | No | Guid | GUID |
| 2 | `AppId` | Edm.String | Yes | App ID | ID de aplicación |
| 3 | `AppType` | Edm.String | Yes | App Type | Tipo de aplicación |
| 4 | `Count` | Edm.Int32 | Yes | Count | Recuento |
| 5 | `Timestamp` | Edm.String | Yes | Timestamp | Marca de tiempo |
| 6 | `Title` | Edm.String | Yes | Title | Título |
| 7 | `Url` | Edm.String | Yes | Url | URL |
| 8 | `UsageArray` | Edm.String | Yes | Usage Array | Matriz de usos |
| 9 | `UserId` | Edm.Int32 | Yes | User ID | ID de usuario |
| 10 | `RecentDay` | Edm.String | Yes | Recent Day | Día reciente |
