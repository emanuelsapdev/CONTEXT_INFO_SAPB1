# ActivityStatuses — Estados de actividades

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ActivityStatuses`
- **Descripción (ES):** Estados de actividades
- **Entity type:** `ActivityStatus` (open type: accepts dynamic/UDF properties)
- **Key:** `StatusId` (Edm.Int32)
- **DB tables (main / lines):** [OCLA](../../Tablas%20SAP%20B1/OCLA.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 3 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ActivityStatuses?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ActivityStatuses/$count` | Contar |
| Get by key | `GET /b1s/v2/ActivityStatuses(1)` | Obtener por clave |
| Create | `POST /b1s/v2/ActivityStatuses` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ActivityStatuses(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ActivityStatuses(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/ActivityStatuses(1)` (only if the B1 object allows removal) | Borrar |

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `StatusDescription` | Edm.String | Yes | Status Description | Descripción del estado |
| 2 | `StatusId` 🔑 | Edm.Int32 | No | Status ID | ID de estado |
| 3 | `StatusName` | Edm.String | Yes | Status Name | Nombre del estado |

## Navigation properties (2)

Use `GET /b1s/v2/ActivityStatuses(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Contacts` | Collection([Contact](../Entidades/Contacts.md)) | [Contacts](Contacts.md) |  | Contactos |
| `Activities` | Collection([Activity](../Entidades/Activities.md)) | [Activities](Activities.md) |  | Actividades |
