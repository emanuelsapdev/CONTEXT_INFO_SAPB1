# SalesOpportunityReasonsSetup — Configuración de motivos de oportunidades

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `SalesOpportunityReasonsSetup`
- **Descripción (ES):** Configuración de motivos de oportunidades
- **Entity type:** `SalesOpportunityReasonSetup`
- **Key:** `SequenceNo` (Edm.Int32)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 3 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/SalesOpportunityReasonsSetup?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/SalesOpportunityReasonsSetup/$count` | Contar |
| Get by key | `GET /b1s/v2/SalesOpportunityReasonsSetup(1)` | Obtener por clave |
| Create | `POST /b1s/v2/SalesOpportunityReasonsSetup` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/SalesOpportunityReasonsSetup(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/SalesOpportunityReasonsSetup(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/SalesOpportunityReasonsSetup(1)` (only if the B1 object allows removal) | Borrar |

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `SequenceNo` 🔑 | Edm.Int32 | No | Sequence Number | Número de secuencia |
| 2 | `Description` | Edm.String | Yes | Description | Descripción |
| 3 | `Sort` | Edm.Int32 | Yes | Sort | Ordenar |

## Navigation properties (1)

Use `GET /b1s/v2/SalesOpportunityReasonsSetup(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `SalesOpportunities` | Collection([SalesOpportunities](../Entidades/SalesOpportunities.md)) | [SalesOpportunities](SalesOpportunities.md) |  | Oportunidades de venta |
