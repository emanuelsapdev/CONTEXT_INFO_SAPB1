# ReportTypes — Tipos de informe

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ReportTypes`
- **Descripción (ES):** Tipos de informe
- **Entity type:** `ReportType`
- **Key:** `TypeCode` (Edm.String)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 6 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ReportTypes?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ReportTypes/$count` | Contar |
| Get by key | `GET /b1s/v2/ReportTypes('value')` | Obtener por clave |
| Create | `POST /b1s/v2/ReportTypes` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ReportTypes('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ReportTypes('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/ReportTypes('value')` (only if the B1 object allows removal) | Borrar |

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TypeCode` 🔑 | Edm.String | No | Type Code | Código de tipo |
| 2 | `TypeName` | Edm.String | Yes | Type Name | Nombre del tipo |
| 3 | `DefaultReportLayout` | Edm.String | Yes | Default Report Layout | Formato de informe predeterminado |
| 4 | `AddonName` | Edm.String | Yes | Addon Name | Nombre del add-on |
| 5 | `AddonFormType` | Edm.String | Yes | Addon Form Type | Tipo de formulario del add-on |
| 6 | `MenuID` | Edm.String | Yes | Menu ID | ID de menú |
