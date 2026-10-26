# WebClientVariantGroups — Cliente web - Grupos de variantes

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `WebClientVariantGroups`
- **Descripción (ES):** Cliente web - Grupos de variantes
- **Entity type:** `WebClientVariantGroup`
- **Key:** `Guid` (Edm.String)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 6 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/WebClientVariantGroups?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/WebClientVariantGroups/$count` | Contar |
| Get by key | `GET /b1s/v2/WebClientVariantGroups('value')` | Obtener por clave |
| Create | `POST /b1s/v2/WebClientVariantGroups` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/WebClientVariantGroups('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/WebClientVariantGroups('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/WebClientVariantGroups('value')` (only if the B1 object allows removal) | Borrar |

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Guid` 🔑 | Edm.String | No | Guid | GUID |
| 2 | `UserId` | Edm.Int32 | Yes | User ID | ID de usuario |
| 3 | `ViewType` | Edm.String | Yes | View Type | Tipo de vista |
| 4 | `ViewId` | Edm.String | Yes | View ID | ID de vista |
| 5 | `ObjectName` | Edm.String | Yes | Object Name | Nombre del objeto |
| 6 | `DefaultVariant` | Edm.String | Yes | Default Variant | Variante predeterminada |
