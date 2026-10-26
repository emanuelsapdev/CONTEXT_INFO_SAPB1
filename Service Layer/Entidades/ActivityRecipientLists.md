# ActivityRecipientLists — Listas de destinatarios de actividades

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ActivityRecipientLists`
- **Descripción (ES):** Listas de destinatarios de actividades
- **Entity type:** `ActivityRecipientList`
- **Key:** `Code` (Edm.Int32)
- **DB tables (main / lines):** [ORCI](../../Tablas%20SAP%20B1/ORCI.md), [RCI1](../../Tablas%20SAP%20B1/RCI1.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 5 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ActivityRecipientLists?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ActivityRecipientLists/$count` | Contar |
| Get by key | `GET /b1s/v2/ActivityRecipientLists(1)` | Obtener por clave |
| Create | `POST /b1s/v2/ActivityRecipientLists` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ActivityRecipientLists(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ActivityRecipientLists(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/ActivityRecipientLists(1)` (only if the B1 object allows removal) | Borrar |

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.Int32 | No | Code | Código |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `Active` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Active | Activo |
| 4 | `IsMultiple` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Multiple | Es múltiple |
| 5 | `ActivityRecipientCollection` | Collection([ActivityRecipient](../Tipos-Complejos/ActivityRecipient.md)) | Yes | Activity Recipient Collection | Colección de destinatarios de la actividad |

## Navigation properties (1)

Use `GET /b1s/v2/ActivityRecipientLists(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Activities` | Collection([Activity](../Entidades/Activities.md)) | [Activities](Activities.md) |  | Actividades |
