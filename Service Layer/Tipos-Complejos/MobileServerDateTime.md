# MobileServerDateTime — Fecha y hora del servidor (móvil)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `MobileServerDateTime`
- **Descripción (ES):** Fecha y hora del servidor (móvil)
- **Description (EN):** Mobile Server Date Time

- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Date` | Edm.DateTimeOffset | Yes | Date | Fecha |
| 2 | `Time` | Edm.TimeOfDay | Yes | Time | Hora |

## Used by (service operations)

- [`MobileAppService_GetCurrentServerDateTime`](../Servicios/MobileAppService.md#mobileappservice_getcurrentserverdatetime)
