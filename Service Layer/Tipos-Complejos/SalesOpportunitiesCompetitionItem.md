# SalesOpportunitiesCompetitionItem — Competencia de la oportunidad de venta

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `SalesOpportunitiesCompetitionItem`
- **Descripción (ES):** Competencia de la oportunidad de venta
- **Description (EN):** Sales Opportunities Competition Item
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 6

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `RowNo` | Edm.Int32 | Yes | Row Number | Número de línea |
| 2 | `Competition` | Edm.Int32 | Yes | Competition | Competencia |
| 3 | `Details` | Edm.String | Yes | Details | Detalles |
| 4 | `SequenceNo` | Edm.Int32 | Yes | Sequence Number | Número de secuencia |
| 5 | `WonOrLost` | Edm.String | Yes | Won Or Lost | Ganada o perdida |
| 6 | `ThreatLevel` | [ThreatLevelEnum](../Enums/ThreatLevelEnum.md) | Yes | Threat Level | Nivel de amenaza |

## Used by (properties)

- [SalesOpportunities](../Entidades/SalesOpportunities.md).`SalesOpportunitiesCompetition`
