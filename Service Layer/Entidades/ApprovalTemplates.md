# ApprovalTemplates — Modelos de autorización

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ApprovalTemplates`
- **Descripción (ES):** Modelos de autorización
- **Entity type:** `ApprovalTemplate`
- **Key:** `Code` (Edm.Int32)
- **DB tables (main / lines):** [OWTM](../../Tablas%20SAP%20B1/OWTM.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 11 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ApprovalTemplates?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ApprovalTemplates/$count` | Contar |
| Get by key | `GET /b1s/v2/ApprovalTemplates(1)` | Obtener por clave |
| Create | `POST /b1s/v2/ApprovalTemplates` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ApprovalTemplates(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ApprovalTemplates(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/ApprovalTemplates(1)` (only if the B1 object allows removal) | Borrar |

## Properties (11)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.Int32 | No | Code | Código |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 4 | `UseTerms` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Use Terms | Usar condiciones |
| 5 | `IsActive` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Active | Está activo |
| 6 | `IsActiveWhenUpdatingDocuments` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Active When Updating Documents | Activo al actualizar documentos |
| 7 | `ApprovalTemplateUsers` | Collection([ApprovalTemplateUser](../Tipos-Complejos/ApprovalTemplateUser.md)) | Yes | Approval Template Users | Usuarios (autores) del modelo de autorización |
| 8 | `ApprovalTemplateStages` | Collection([ApprovalTemplateStage](../Tipos-Complejos/ApprovalTemplateStage.md)) | Yes | Approval Template Stages | Etapas del modelo de autorización |
| 9 | `ApprovalTemplateDocuments` | Collection([ApprovalTemplateDocument](../Tipos-Complejos/ApprovalTemplateDocument.md)) | Yes | Approval Template Documents | Documentos del modelo de autorización |
| 10 | `ApprovalTemplateTerms` | Collection([ApprovalTemplateTerm](../Tipos-Complejos/ApprovalTemplateTerm.md)) | Yes | Approval Template Terms | Condiciones del modelo de autorización |
| 11 | `ApprovalTemplateQueries` | Collection([ApprovalTemplateQuery](../Tipos-Complejos/ApprovalTemplateQuery.md)) | Yes | Approval Template Queries | Consultas del modelo de autorización |

## Navigation properties (1)

Use `GET /b1s/v2/ApprovalTemplates(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `ApprovalRequests` | Collection([ApprovalRequest](../Entidades/ApprovalRequests.md)) | [ApprovalRequests](ApprovalRequests.md) |  | Solicitudes de autorización |
