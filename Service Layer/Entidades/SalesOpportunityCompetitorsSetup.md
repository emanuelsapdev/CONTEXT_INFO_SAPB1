# SalesOpportunityCompetitorsSetup — Configuración de competidores de oportunidades

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `SalesOpportunityCompetitorsSetup`
- **Descripción (ES):** Configuración de competidores de oportunidades
- **Entity type:** `SalesOpportunityCompetitorSetup`
- **Key:** `SequenceNo` (Edm.Int32)
- **DB tables (main / lines):** [OCMT](../../Tablas%20SAP%20B1/OCMT.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 4 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/SalesOpportunityCompetitorsSetup?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/SalesOpportunityCompetitorsSetup/$count` | Contar |
| Get by key | `GET /b1s/v2/SalesOpportunityCompetitorsSetup(1)` | Obtener por clave |
| Create | `POST /b1s/v2/SalesOpportunityCompetitorsSetup` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/SalesOpportunityCompetitorsSetup(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/SalesOpportunityCompetitorsSetup(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/SalesOpportunityCompetitorsSetup(1)` (only if the B1 object allows removal) | Borrar |

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `SequenceNo` 🔑 | Edm.Int32 | No | Sequence Number | Número de secuencia |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `ThreatLevel` | [ThreatLevelEnum](../Enums/ThreatLevelEnum.md) | Yes | Threat Level | Nivel de amenaza |
| 4 | `Details` | Edm.String | Yes | Details | Detalles |
