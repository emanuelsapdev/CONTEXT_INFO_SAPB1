# WebClientNotifications — Cliente web - Notificaciones

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `WebClientNotifications`
- **Descripción (ES):** Cliente web - Notificaciones
- **Entity type:** `WebClientNotification`
- **Key:** `Guid` (Edm.String)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 6 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/WebClientNotifications?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/WebClientNotifications/$count` | Contar |
| Get by key | `GET /b1s/v2/WebClientNotifications('value')` | Obtener por clave |
| Create | `POST /b1s/v2/WebClientNotifications` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/WebClientNotifications('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/WebClientNotifications('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/WebClientNotifications('value')` (only if the B1 object allows removal) | Borrar |

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Guid` 🔑 | Edm.String | No | Guid | GUID |
| 2 | `UserId` | Edm.Int32 | Yes | User ID | ID de usuario |
| 3 | `ActivityDate` | Edm.DateTimeOffset | Yes | Activity Date | Fecha de la actividad |
| 4 | `ReadStatus` | Edm.String | Yes | Read Status | Estado de lectura |
| 5 | `IsDismissed` | Edm.String | Yes | Is Dismissed | Está descartado |
| 6 | `NotiType` | Edm.Int32 | Yes | Noti Type | Tipo de notificación |
