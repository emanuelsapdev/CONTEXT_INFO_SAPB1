# TechnicianSchedulings — Programaciones de técnicos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `TechnicianSchedulings`
- **Descripción (ES):** Programaciones de técnicos
- **Description (EN):** Technician Schedulings

- **Properties:** 5

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ServiceCallID` | Edm.Int32 | Yes | Service Call ID | ID de llamada de servicio |
| 2 | `SchedulingLineNum` | Edm.Int32 | Yes | Scheduling Line Number | Línea de programación |
| 3 | `StartDate` | Edm.DateTimeOffset | Yes | Start Date | Fecha de inicio |
| 4 | `EndDate` | Edm.DateTimeOffset | Yes | End Date | Fecha de fin |
| 5 | `IsClosed` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Closed | Está cerrado |

## Used by (service operations)

- [`MobileAppService_GetTechnicianSchedulings`](../Servicios/MobileAppService.md#mobileappservice_gettechnicianschedulings)
