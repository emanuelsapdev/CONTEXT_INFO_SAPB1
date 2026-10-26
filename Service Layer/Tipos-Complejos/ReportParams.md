# ReportParams — Parámetros de informe

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ReportParams`
- **Descripción (ES):** Parámetros de informe
- **Description (EN):** Report Parameters

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ReportCode` | Edm.String | Yes | Report Code | Código de informe |
| 2 | `UserID` | Edm.Int32 | Yes | User ID | ID de usuario |
| 3 | `CardCode` | Edm.String | Yes | Card Code | Código del socio de negocios |

## Used by (service operations)

- [`ReportLayoutsService_GetDefaultReport`](../Servicios/ReportLayoutsService.md#reportlayoutsservice_getdefaultreport)
- [`ReportLayoutsService_GetDefaultReportLayout`](../Servicios/ReportLayoutsService.md#reportlayoutsservice_getdefaultreportlayout)
- [`ReportLayoutsService_GetReportLayoutList`](../Servicios/ReportLayoutsService.md#reportlayoutsservice_getreportlayoutlist)
