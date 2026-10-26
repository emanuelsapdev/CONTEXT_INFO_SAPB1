# ApprovalStages — Etapas de autorización

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ApprovalStages`
- **Descripción (ES):** Etapas de autorización
- **Entity type:** `ApprovalStage`
- **Key:** `Code` (Edm.Int32)
- **DB tables (main / lines):** [OWST](../../Tablas%20SAP%20B1/OWST.md), [WST1](../../Tablas%20SAP%20B1/WST1.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 5 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ApprovalStages?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ApprovalStages/$count` | Contar |
| Get by key | `GET /b1s/v2/ApprovalStages(1)` | Obtener por clave |
| Create | `POST /b1s/v2/ApprovalStages` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ApprovalStages(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ApprovalStages(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/ApprovalStages(1)` (only if the B1 object allows removal) | Borrar |

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.Int32 | No | Code | Código |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `NoOfApproversRequired` | Edm.Int32 | Yes | Number Of Approvers Required | Cantidad de autorizadores requeridos |
| 4 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 5 | `ApprovalStageApprovers` | Collection([ApprovalStageApprover](../Tipos-Complejos/ApprovalStageApprover.md)) | Yes | Approval Stage Approvers | Autorizadores de la etapa |

## Navigation properties (1)

Use `GET /b1s/v2/ApprovalStages(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `ApprovalRequests` | Collection([ApprovalRequest](../Entidades/ApprovalRequests.md)) | [ApprovalRequests](ApprovalRequests.md) |  | Solicitudes de autorización |
