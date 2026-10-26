# FinancePeriodParams — Parámetros de período contable

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `FinancePeriodParams`
- **Descripción (ES):** Parámetros de período contable
- **Description (EN):** Finance Period Parameters

- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsoluteEntry` | Edm.Int32 | Yes | Absolute Entry | Entrada absoluta (ID interno) |
| 2 | `PeriodIndicator` | Edm.String | Yes | Period Indicator | Indicador de período |

## Used by (service operations)

- [`CompanyService_CreatePeriodWithFinanceParams`](../Servicios/CompanyService.md#companyservice_createperiodwithfinanceparams)
- [`CompanyService_GetFinancePeriod`](../Servicios/CompanyService.md#companyservice_getfinanceperiod)
- [`CompanyService_RemoveFinancePeriod`](../Servicios/CompanyService.md#companyservice_removefinanceperiod)
