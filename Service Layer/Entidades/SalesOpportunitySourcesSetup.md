# SalesOpportunitySourcesSetup — Configuración de fuentes de información de oportunidades

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `SalesOpportunitySourcesSetup`
- **Descripción (ES):** Configuración de fuentes de información de oportunidades
- **Entity type:** `SalesOpportunitySourceSetup`
- **Key:** `SequenceNo` (Edm.Int32)
- **DB tables (main / lines):** [OOSR](../../Tablas%20SAP%20B1/OOSR.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 3 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/SalesOpportunitySourcesSetup?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/SalesOpportunitySourcesSetup/$count` | Contar |
| Get by key | `GET /b1s/v2/SalesOpportunitySourcesSetup(1)` | Obtener por clave |
| Create | `POST /b1s/v2/SalesOpportunitySourcesSetup` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/SalesOpportunitySourcesSetup(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/SalesOpportunitySourcesSetup(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/SalesOpportunitySourcesSetup(1)` (only if the B1 object allows removal) | Borrar |

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `SequenceNo` 🔑 | Edm.Int32 | No | Sequence Number | Número de secuencia |
| 2 | `Description` | Edm.String | Yes | Description | Descripción |
| 3 | `Sort` | Edm.Int32 | Yes | Sort | Ordenar |

## Navigation properties (1)

Use `GET /b1s/v2/SalesOpportunitySourcesSetup(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `SalesOpportunities` | Collection([SalesOpportunities](../Entidades/SalesOpportunities.md)) | [SalesOpportunities](SalesOpportunities.md) |  | Oportunidades de venta |
