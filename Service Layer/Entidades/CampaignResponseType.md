# CampaignResponseType — Tipos de respuesta de campaña

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `CampaignResponseType`
- **Descripción (ES):** Tipos de respuesta de campaña
- **Entity type:** `CampaignResponseType`
- **Key:** `ResponseType` (Edm.String)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 3 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/CampaignResponseType?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/CampaignResponseType/$count` | Contar |
| Get by key | `GET /b1s/v2/CampaignResponseType('value')` | Obtener por clave |
| Create | `POST /b1s/v2/CampaignResponseType` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/CampaignResponseType('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/CampaignResponseType('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/CampaignResponseType('value')` (only if the B1 object allows removal) | Borrar |

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ResponseTypeDescription` | Edm.String | Yes | Response Type Description | Descripción del tipo de respuesta |
| 2 | `ResponseType` 🔑 | Edm.String | No | Response Type | Tipo de respuesta |
| 3 | `IsActive` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Active | Está activo |
