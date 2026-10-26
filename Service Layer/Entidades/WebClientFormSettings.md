# WebClientFormSettings — Cliente web - Configuración de formularios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `WebClientFormSettings`
- **Descripción (ES):** Cliente web - Configuración de formularios
- **Entity type:** `WebClientFormSetting`
- **Key:** `Guid` (Edm.String)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 5 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/WebClientFormSettings?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/WebClientFormSettings/$count` | Contar |
| Get by key | `GET /b1s/v2/WebClientFormSettings('value')` | Obtener por clave |
| Create | `POST /b1s/v2/WebClientFormSettings` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/WebClientFormSettings('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/WebClientFormSettings('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/WebClientFormSettings('value')` (only if the B1 object allows removal) | Borrar |

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Guid` 🔑 | Edm.String | No | Guid | GUID |
| 2 | `FormId` | Edm.String | Yes | Form ID | ID de formulario |
| 3 | `UserId` | Edm.Int32 | Yes | User ID | ID de usuario |
| 4 | `DocObjectCode` | Edm.String | Yes | Document Object Code | Código de objeto del documento |
| 5 | `WebClientFormSettingItems` | Collection([WebClientFormSettingItem](../Tipos-Complejos/WebClientFormSettingItem.md)) | Yes | Web Client Form Setting Items | Elementos de configuración de formulario del cliente web |
