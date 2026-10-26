# ServiceAppReportParams — Parámetros de informe de la app de servicio

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ServiceAppReportParams`
- **Descripción (ES):** Parámetros de informe de la app de servicio
- **Description (EN):** Service App Report Parameters

- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` | Edm.Int32 | Yes | Code | Código |
| 2 | `ReportChoice` | [MobileAppReportChoiceEnum](../Enums/MobileAppReportChoiceEnum.md) | Yes | Report Choice | Selección de informe |

## Used by (service operations)

- [`MobileAppService_GetServiceAppReport`](../Servicios/MobileAppService.md#mobileappservice_getserviceappreport)
- [`MobileAppService_GetServiceAppReportContent`](../Servicios/MobileAppService.md#mobileappservice_getserviceappreportcontent)
- [`MobileAppService_UpdateServiceAppReportContent`](../Servicios/MobileAppService.md#mobileappservice_updateserviceappreportcontent)
