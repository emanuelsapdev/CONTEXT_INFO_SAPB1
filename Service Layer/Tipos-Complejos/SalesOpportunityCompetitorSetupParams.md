# SalesOpportunityCompetitorSetupParams — Parámetros de configuración de competidores de oportunidades

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `SalesOpportunityCompetitorSetupParams`
- **Descripción (ES):** Parámetros de configuración de competidores de oportunidades
- **Description (EN):** Sales Opportunity Competitor Setup Parameters

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `SequenceNo` | Edm.Int32 | Yes | Sequence Number | Número de secuencia |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `ThreatLevel` | [ThreatLevelEnum](../Enums/ThreatLevelEnum.md) | Yes | Threat Level | Nivel de amenaza |

## Used by (service operations)

- [`SalesOpportunityCompetitorsSetupService_GetSalesOpportunityCompetitorSetupList`](../Servicios/SalesOpportunityCompetitorsSetupService.md#salesopportunitycompetitorssetupservice_getsalesopportunitycompetitorsetuplist)
