# FinancePeriod — Período contable

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `FinancePeriod`
- **Descripción (ES):** Período contable
- **Description (EN):** Finance Period

- **Properties:** 15

## Properties (15)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsoluteEntry` | Edm.Int32 | Yes | Absolute Entry | Entrada absoluta (ID interno) |
| 2 | `PeriodCode` | Edm.String | Yes | Period Code | Código de período |
| 3 | `PeriodName` | Edm.String | Yes | Period Name | Nombre del período |
| 4 | `PostingDateFrom` | Edm.DateTimeOffset | Yes | Posting Date From | Fecha de contabilización desde |
| 5 | `PostingDateTo` | Edm.DateTimeOffset | Yes | Posting Date To | Fecha de contabilización hasta |
| 6 | `ValueDateFrom` | Edm.DateTimeOffset | Yes | Value Date From | Fecha valor desde |
| 7 | `ValueDateTo` | Edm.DateTimeOffset | Yes | Value Date To | Fecha valor hasta |
| 8 | `TaxDateFrom` | Edm.DateTimeOffset | Yes | Tax Date From | Fecha de impuestos desde |
| 9 | `TaxDateTo` | Edm.DateTimeOffset | Yes | Tax Date To | Fecha de impuestos hasta |
| 10 | `ActiveforFeed` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Activefor Feed | Activo para alimentación (feed) |
| 11 | `Locked` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Locked | Bloqueado |
| 12 | `AdditionalSubPeriods` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Additional Sub Periods | Subperíodos adicionales |
| 13 | `PeriodIndicator` | Edm.String | Yes | Period Indicator | Indicador de período |
| 14 | `SubNum` | Edm.Int32 | Yes | Sub Number | Subnúmero |
| 15 | `PeriodStatus` | [PeriodStatusEnum](../Enums/PeriodStatusEnum.md) | Yes | Period Status | Estado del período |

## Used by (service operations)

- [`CompanyService_GetFinancePeriod`](../Servicios/CompanyService.md#companyservice_getfinanceperiod)
- [`CompanyService_GetFinancePeriods`](../Servicios/CompanyService.md#companyservice_getfinanceperiods)
- [`CompanyService_UpdateFinancePeriod`](../Servicios/CompanyService.md#companyservice_updatefinanceperiod)
