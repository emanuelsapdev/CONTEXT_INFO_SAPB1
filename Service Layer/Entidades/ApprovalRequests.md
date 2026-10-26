# ApprovalRequests — Solicitudes de autorización

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ApprovalRequests`
- **Descripción (ES):** Solicitudes de autorización
- **Entity type:** `ApprovalRequest`
- **Key:** `Code` (Edm.Int32)
- **DB tables (main / lines):** [OWDD](../../Tablas%20SAP%20B1/OWDD.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 15 · **Navigation properties:** 3 · **Bound actions:** 2

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ApprovalRequests?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ApprovalRequests/$count` | Contar |
| Get by key | `GET /b1s/v2/ApprovalRequests(1)` | Obtener por clave |
| Create | `POST /b1s/v2/ApprovalRequests` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ApprovalRequests(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ApprovalRequests(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/ApprovalRequests(1)` (only if the B1 object allows removal) | Borrar |
| Action `CancelApprovalRequest` | `POST /b1s/v2/ApprovalRequests(1)/CancelApprovalRequest` | Cancelar solicitud de autorización |
| Action `RestoreApprovalRequest` | `POST /b1s/v2/ApprovalRequests(1)/RestoreApprovalRequest` | Restaurar solicitud de autorización |

## Properties (15)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.Int32 | No | Code | Código |
| 2 | `ApprovalTemplatesID` | Edm.Int32 | Yes | Approval Templates ID | ID del modelo de autorización |
| 3 | `ObjectType` | Edm.String | Yes | Object Type | Tipo de objeto |
| 4 | `IsDraft` | Edm.String | Yes | Is Draft | Es borrador |
| 5 | `ObjectEntry` | Edm.Int32 | Yes | Object Entry | Entrada del objeto |
| 6 | `Status` | [BoApprovalRequestStatusEnum](../Enums/BoApprovalRequestStatusEnum.md) | Yes | Status | Estado |
| 7 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 8 | `CurrentStage` | Edm.Int32 | Yes | Current Stage | Etapa actual |
| 9 | `OriginatorID` | Edm.Int32 | Yes | Originator ID | ID del originador |
| 10 | `CreationDate` | Edm.DateTimeOffset | Yes | Creation Date | Fecha de creación |
| 11 | `CreationTime` | Edm.TimeOfDay | Yes | Creation Time | Hora de creación |
| 12 | `DraftEntry` | Edm.Int32 | Yes | Draft Entry | Entrada del borrador |
| 13 | `DraftType` | Edm.String | Yes | Draft Type | Tipo de borrador |
| 14 | `ApprovalRequestLines` | Collection([ApprovalRequestLine](../Tipos-Complejos/ApprovalRequestLine.md)) | Yes | Approval Request Lines | Líneas de la solicitud de autorización |
| 15 | `ApprovalRequestDecisions` | Collection([ApprovalRequestDecision](../Tipos-Complejos/ApprovalRequestDecision.md)) | Yes | Approval Request Decisions | Decisiones de la solicitud de autorización |

## Navigation properties (3)

Use `GET /b1s/v2/ApprovalRequests(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `ApprovalTemplate` | [ApprovalTemplate](../Entidades/ApprovalTemplates.md) | [ApprovalTemplates](ApprovalTemplates.md) | ApprovalTemplatesID → Code | Modelos de autorización |
| `ApprovalStage` | [ApprovalStage](../Entidades/ApprovalStages.md) | [ApprovalStages](ApprovalStages.md) | CurrentStage → Code | Etapas de autorización |
| `User` | [User](../Entidades/Users.md) | [Users](Users.md) | OriginatorID → InternalKey | Usuario |

## Bound actions (2)

### CancelApprovalRequest

- **Descripción (ES):** Cancelar solicitud de autorización
- **Request:** `POST /b1s/v2/ApprovalRequests(1)/CancelApprovalRequest`

### RestoreApprovalRequest

- **Descripción (ES):** Restaurar solicitud de autorización
- **Request:** `POST /b1s/v2/ApprovalRequests(1)/RestoreApprovalRequest`

