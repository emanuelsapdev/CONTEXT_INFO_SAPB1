# ReportLayoutParams — Parámetros de formato de informe

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ReportLayoutParams`
- **Descripción (ES):** Parámetros de formato de informe
- **Description (EN):** Report Layout Parameters

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LayoutCode` | Edm.String | Yes | Layout Code | Código de formato |
| 2 | `LayoutName` | Edm.String | Yes | Layout Name | Nombre de formato |
| 3 | `Category` | [ReportLayoutCategoryEnum](../Enums/ReportLayoutCategoryEnum.md) | Yes | Category | Categoría |

## Used by (service operations)

- [`ReportLayoutsService_AddReportLayout`](../Servicios/ReportLayoutsService.md#reportlayoutsservice_addreportlayout)
- [`ReportLayoutsService_AddReportLayoutToMenu`](../Servicios/ReportLayoutsService.md#reportlayoutsservice_addreportlayouttomenu)
- [`ReportLayoutsService_DeleteReportLayout`](../Servicios/ReportLayoutsService.md#reportlayoutsservice_deletereportlayout)
- [`ReportLayoutsService_DeleteReportLayoutAndMenu`](../Servicios/ReportLayoutsService.md#reportlayoutsservice_deletereportlayoutandmenu)
- [`ReportLayoutsService_GetReportLayout`](../Servicios/ReportLayoutsService.md#reportlayoutsservice_getreportlayout)
- [`ReportLayoutsService_GetReportLayoutList`](../Servicios/ReportLayoutsService.md#reportlayoutsservice_getreportlayoutlist)
