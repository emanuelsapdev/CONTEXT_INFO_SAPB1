# WebClientLaunchpads — Cliente web - Launchpads

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `WebClientLaunchpads`
- **Descripción (ES):** Cliente web - Launchpads
- **Entity type:** `WebClientLaunchpad`
- **Key:** `Guid` (Edm.String)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 6 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/WebClientLaunchpads?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/WebClientLaunchpads/$count` | Contar |
| Get by key | `GET /b1s/v2/WebClientLaunchpads('value')` | Obtener por clave |
| Create | `POST /b1s/v2/WebClientLaunchpads` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/WebClientLaunchpads('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/WebClientLaunchpads('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/WebClientLaunchpads('value')` (only if the B1 object allows removal) | Borrar |

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Guid` 🔑 | Edm.String | No | Guid | GUID |
| 2 | `UserId` | Edm.Int32 | Yes | User ID | ID de usuario |
| 3 | `ThemeId` | Edm.String | Yes | Theme ID | ID de tema |
| 4 | `DisplayQuickView` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Display Quick View | Mostrar vista rápida |
| 5 | `NotificationShowDays` | Edm.Int32 | Yes | Notification Show Days | Días para mostrar notificaciones |
| 6 | `WebClientLaunchpadGroups` | Collection([WebClientLaunchpadGroup](../Tipos-Complejos/WebClientLaunchpadGroup.md)) | Yes | Web Client Launchpad Groups | Grupos del launchpad del cliente web |
