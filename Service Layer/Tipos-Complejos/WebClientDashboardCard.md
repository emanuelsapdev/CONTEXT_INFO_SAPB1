# WebClientDashboardCard — Tarjetas del dashboard del cliente web

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `WebClientDashboardCard`
- **Descripción (ES):** Tarjetas del dashboard del cliente web
- **Description (EN):** Web Client Dashboard Card

- **Properties:** 5

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Guid` | Edm.String | Yes | Guid | GUID |
| 2 | `UserId` | Edm.Int32 | Yes | User ID | ID de usuario |
| 3 | `Content` | Edm.String | Yes | Content | Contenido |
| 4 | `Sys` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | (system currency) | Sistema |
| 5 | `Version` | Edm.String | Yes | Version | Versión |

## Used by (properties)

- [WebClientDashboard](../Entidades/WebClientDashboards.md).`WebClientDashboardCards`
