# ActivitySubjects — Asuntos de actividades

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ActivitySubjects`
- **Descripción (ES):** Asuntos de actividades
- **Entity type:** `ActivitySubject`
- **Key:** `Code` (Edm.Int32)
- **DB tables (main / lines):** [OCLS](../../Tablas%20SAP%20B1/OCLS.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 4 · **Navigation properties:** 3 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ActivitySubjects?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ActivitySubjects/$count` | Contar |
| Get by key | `GET /b1s/v2/ActivitySubjects(1)` | Obtener por clave |
| Create | `POST /b1s/v2/ActivitySubjects` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ActivitySubjects(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ActivitySubjects(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/ActivitySubjects(1)` (only if the B1 object allows removal) | Borrar |

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.Int32 | No | Code | Código |
| 2 | `Description` | Edm.String | Yes | Description | Descripción |
| 3 | `ActivityType` | Edm.Int32 | Yes | Activity Type | Tipo de actividad |
| 4 | `IsActive` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Active | Está activo |

## Navigation properties (3)

Use `GET /b1s/v2/ActivitySubjects(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `ActivityType2` | [ActivityType](../Entidades/ActivityTypes.md) | [ActivityTypes](ActivityTypes.md) | ActivityType → Code | Tipos de actividades |
| `Contacts` | Collection([Contact](../Entidades/Contacts.md)) | [Contacts](Contacts.md) |  | Contactos |
| `Activities` | Collection([Activity](../Entidades/Activities.md)) | [Activities](Activities.md) |  | Actividades |

## Service operations that use this type

- [`ActivitySubjectService_GetListByTypeCode`](../Servicios/ActivitySubjectService.md#activitysubjectservice_getlistbytypecode)
