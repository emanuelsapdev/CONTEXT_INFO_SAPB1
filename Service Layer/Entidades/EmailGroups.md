# EmailGroups — Grupos de correo electrónico

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `EmailGroups`
- **Descripción (ES):** Grupos de correo electrónico
- **Entity type:** `EmailGroup`
- **Key:** `EmailGroupCode` (Edm.String)
- **DB tables (main / lines):** [OEGP](../../Tablas%20SAP%20B1/OEGP.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 2 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/EmailGroups?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/EmailGroups/$count` | Contar |
| Get by key | `GET /b1s/v2/EmailGroups('value')` | Obtener por clave |
| Create | `POST /b1s/v2/EmailGroups` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/EmailGroups('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/EmailGroups('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/EmailGroups('value')` (only if the B1 object allows removal) | Borrar |

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `EmailGroupCode` 🔑 | Edm.String | No | Email Group Code | Código de grupo de correo |
| 2 | `EmailGroupName` | Edm.String | Yes | Email Group Name | Nombre del grupo de correo |
