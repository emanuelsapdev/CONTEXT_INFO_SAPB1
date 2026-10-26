# KnowledgeBaseSolutions — Soluciones de la base de conocimiento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `KnowledgeBaseSolutions`
- **Descripción (ES):** Soluciones de la base de conocimiento
- **Entity type:** `KnowledgeBaseSolution` (open type: accepts dynamic/UDF properties)
- **Key:** `SolutionCode` (Edm.Int32)
- **DB tables (main / lines):** [OSLT](../../Tablas%20SAP%20B1/OSLT.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 13 · **Navigation properties:** 3 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/KnowledgeBaseSolutions?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/KnowledgeBaseSolutions/$count` | Contar |
| Get by key | `GET /b1s/v2/KnowledgeBaseSolutions(1)` | Obtener por clave |
| Create | `POST /b1s/v2/KnowledgeBaseSolutions` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/KnowledgeBaseSolutions(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/KnowledgeBaseSolutions(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/KnowledgeBaseSolutions(1)` (only if the B1 object allows removal) | Borrar |

## Properties (13)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |
| 2 | `Status` | Edm.Int32 | Yes | Status | Estado |
| 3 | `Owner` | Edm.Int32 | Yes | Owner | Titular |
| 4 | `CreatedBy` | Edm.Int32 | Yes | Created By | Creado por |
| 5 | `CreationDate` | Edm.DateTimeOffset | Yes | Creation Date | Fecha de creación |
| 6 | `LastUpdatedBy` | Edm.Int32 | Yes | Last Updated By | Actualizado por última vez por |
| 7 | `LastUpdateDate` | Edm.DateTimeOffset | Yes | Last Update Date | Fecha de la última actualización |
| 8 | `Solution` | Edm.String | Yes | Solution | Solución |
| 9 | `Symptom` | Edm.String | Yes | Symptom | Síntoma |
| 10 | `Cause` | Edm.String | Yes | Cause | Causa |
| 11 | `Description` | Edm.String | Yes | Description | Descripción |
| 12 | `SolutionCode` 🔑 | Edm.Int32 | No | Solution Code | Código de solución |
| 13 | `AttachmentEntry` | Edm.Int32 | Yes | Attachment Entry | Entrada de anexo (ID) |

## Navigation properties (3)

Use `GET /b1s/v2/KnowledgeBaseSolutions(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Item` | [Item](../Entidades/Items.md) | [Items](Items.md) | ItemCode → ItemCode | Artículos |
| `ServiceCallSolutionStatus` | [ServiceCallSolutionStatus](../Entidades/ServiceCallSolutionStatus.md) | [ServiceCallSolutionStatus](ServiceCallSolutionStatus.md) | Status → StatusId | Estados de soluciones de llamadas de servicio |
| `User` | [User](../Entidades/Users.md) | [Users](Users.md) | Owner → InternalKey | Usuario |
