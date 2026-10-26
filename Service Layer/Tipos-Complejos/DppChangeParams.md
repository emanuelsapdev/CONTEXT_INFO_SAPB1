# DppChangeParams — Parámetros de cambio de protección de datos personales

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DppChangeParams`
- **Descripción (ES):** Parámetros de cambio de protección de datos personales
- **Description (EN):** Dpp Change Parameters

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `FromDate` | Edm.DateTimeOffset | Yes | From Date | Fecha desde |
| 2 | `FromTime` | Edm.TimeOfDay | Yes | From Time | Hora desde |
| 3 | `HasChanged` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Has Changed | Ha cambiado |

## Used by (service operations)

- [`MobileAppService_GetDppChangeParams`](../Servicios/MobileAppService.md#mobileappservice_getdppchangeparams)
