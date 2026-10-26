# ActivityLocations — Lugares de actividades

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ActivityLocations`
- **Descripción (ES):** Lugares de actividades
- **Entity type:** `ActivityLocation` (open type: accepts dynamic/UDF properties)
- **Key:** `Code` (Edm.Int32)
- **DB tables (main / lines):** [OCLO](../../Tablas%20SAP%20B1/OCLO.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 2 · **Navigation properties:** 3 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ActivityLocations?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ActivityLocations/$count` | Contar |
| Get by key | `GET /b1s/v2/ActivityLocations(1)` | Obtener por clave |
| Create | `POST /b1s/v2/ActivityLocations` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ActivityLocations(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ActivityLocations(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/ActivityLocations(1)` (only if the B1 object allows removal) | Borrar |

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.Int32 | No | Code | Código |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |

## Navigation properties (3)

Use `GET /b1s/v2/ActivityLocations(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `ServiceCalls` | Collection([ServiceCall](../Entidades/ServiceCalls.md)) | [ServiceCalls](ServiceCalls.md) |  | Llamadas de servicio |
| `Contacts` | Collection([Contact](../Entidades/Contacts.md)) | [Contacts](Contacts.md) |  | Contactos |
| `Activities` | Collection([Activity](../Entidades/Activities.md)) | [Activities](Activities.md) |  | Actividades |
