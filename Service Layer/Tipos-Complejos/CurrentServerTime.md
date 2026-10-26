# CurrentServerTime — Hora actual del servidor

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `CurrentServerTime`
- **Descripción (ES):** Hora actual del servidor
- **Description (EN):** Current Server Time

- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `CurrentDate` | Edm.DateTimeOffset | Yes | Current Date | Fecha actual |
| 2 | `CurrentTime` | Edm.TimeOfDay | Yes | Current Time | Hora actual |

## Used by (service operations)

- [`CompanyService_GetCurrentServerTime`](../Servicios/CompanyService.md#companyservice_getcurrentservertime)
