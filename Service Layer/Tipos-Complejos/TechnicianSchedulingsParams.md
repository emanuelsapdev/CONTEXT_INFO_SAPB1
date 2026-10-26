# TechnicianSchedulingsParams — Parámetros de programaciones de técnicos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `TechnicianSchedulingsParams`
- **Descripción (ES):** Parámetros de programaciones de técnicos
- **Description (EN):** Technician Schedulings Parameters

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Technician` | Edm.Int32 | Yes | Technician | Técnico |
| 2 | `StartDate` | Edm.DateTimeOffset | Yes | Start Date | Fecha de inicio |
| 3 | `EndDate` | Edm.DateTimeOffset | Yes | End Date | Fecha de fin |

## Used by (service operations)

- [`MobileAppService_GetTechnicianSchedulings`](../Servicios/MobileAppService.md#mobileappservice_gettechnicianschedulings)
