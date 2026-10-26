# ServiceTaxPostingParams — Parámetros de contabilización de impuesto de servicios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ServiceTaxPostingParams`
- **Descripción (ES):** Parámetros de contabilización de impuesto de servicios
- **Description (EN):** Service Tax Posting Parameters

- **Properties:** 1

## Properties (1)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |

## Used by (service operations)

- [`ServiceTaxPostingService_GetTaxableDeliveries`](../Servicios/ServiceTaxPostingService.md#servicetaxpostingservice_gettaxabledeliveries)
- [`ServiceTaxPostingService_PostServiceTax`](../Servicios/ServiceTaxPostingService.md#servicetaxpostingservice_postservicetax)
