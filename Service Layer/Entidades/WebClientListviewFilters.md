# WebClientListviewFilters — Cliente web - Filtros de vista de lista

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `WebClientListviewFilters`
- **Descripción (ES):** Cliente web - Filtros de vista de lista
- **Entity type:** `WebClientListviewFilter`
- **Key:** `Guid` (Edm.String)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 5 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/WebClientListviewFilters?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/WebClientListviewFilters/$count` | Contar |
| Get by key | `GET /b1s/v2/WebClientListviewFilters('value')` | Obtener por clave |
| Create | `POST /b1s/v2/WebClientListviewFilters` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/WebClientListviewFilters('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/WebClientListviewFilters('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/WebClientListviewFilters('value')` (only if the B1 object allows removal) | Borrar |

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Guid` 🔑 | Edm.String | No | Guid | GUID |
| 2 | `UserId` | Edm.Int32 | Yes | User ID | ID de usuario |
| 3 | `TableName` | Edm.String | Yes | Table Name | Nombre de la tabla |
| 4 | `FilterName` | Edm.String | Yes | Filter Name | Nombre del filtro |
| 5 | `WebClientListviewFilterConditions` | Collection([WebClientListviewFilterCondition](../Tipos-Complejos/WebClientListviewFilterCondition.md)) | Yes | Web Client Listview Filter Conditions | Condiciones del filtro de vista de lista |
