# ServiceAppReport — Informe de la app de servicio

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ServiceAppReport`
- **Descripción (ES):** Informe de la app de servicio
- **Description (EN):** Service App Report

- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` | Edm.Int32 | Yes | Code | Código |
| 2 | `SystemReportName` | Edm.String | Yes | System Report Name | Nombre del informe del sistema |
| 3 | `CustomizedReportName` | Edm.String | Yes | Customized Report Name | Nombre del informe personalizado |
| 4 | `ReportChoice` | [MobileAppReportChoiceEnum](../Enums/MobileAppReportChoiceEnum.md) | Yes | Report Choice | Selección de informe |

## Used by (service operations)

- [`MobileAppService_GetServiceAppReport`](../Servicios/MobileAppService.md#mobileappservice_getserviceappreport)
- [`MobileAppService_UpdateServiceAppReport`](../Servicios/MobileAppService.md#mobileappservice_updateserviceappreport)
