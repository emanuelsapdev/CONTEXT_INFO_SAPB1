# Queue — Colas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `Queue`
- **Descripción (ES):** Colas
- **Entity type:** `Queue` (open type: accepts dynamic/UDF properties)
- **Key:** `QueueID` (Edm.String)
- **DB tables (main / lines):** [OQUE](../../Tablas%20SAP%20B1/OQUE.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 6 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/Queue?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/Queue/$count` | Contar |
| Get by key | `GET /b1s/v2/Queue('value')` | Obtener por clave |
| Create | `POST /b1s/v2/Queue` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/Queue('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/Queue('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/Queue('value')` (only if the B1 object allows removal) | Borrar |

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `QueueID` 🔑 | Edm.String | No | Queue ID | ID de cola |
| 2 | `Description` | Edm.String | Yes | Description | Descripción |
| 3 | `Inactive` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Inactive | Inactivo |
| 4 | `QueueManager` | Edm.Int32 | Yes | Queue Manager | Responsable de la cola |
| 5 | `QueueEmail` | Edm.String | Yes | Queue Email | Correo de la cola |
| 6 | `QueueMembers` | Collection([QueueMember](../Tipos-Complejos/QueueMember.md)) | Yes | Queue Members | Miembros de la cola |

## Navigation properties (2)

Use `GET /b1s/v2/Queue('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `ServiceCalls` | Collection([ServiceCall](../Entidades/ServiceCalls.md)) | [ServiceCalls](ServiceCalls.md) |  | Llamadas de servicio |
| `User` | [User](../Entidades/Users.md) | [Users](Users.md) | QueueManager → InternalKey | Usuario |
