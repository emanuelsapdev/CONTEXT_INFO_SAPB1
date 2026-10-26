# DefaultReportParams — Parámetros de informe predeterminado

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DefaultReportParams`
- **Descripción (ES):** Parámetros de informe predeterminado
- **Description (EN):** Default Report Parameters

- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ReportCode` | Edm.String | Yes | Report Code | Código de informe |
| 2 | `LayoutCode` | Edm.String | Yes | Layout Code | Código de formato |
| 3 | `UserID` | Edm.Int32 | Yes | User ID | ID de usuario |
| 4 | `CardCode` | Edm.String | Yes | Card Code | Código del socio de negocios |

## Used by (service operations)

- [`ReportLayoutsService_GetDefaultReport`](../Servicios/ReportLayoutsService.md#reportlayoutsservice_getdefaultreport)
- [`ReportLayoutsService_SetDefaultReport`](../Servicios/ReportLayoutsService.md#reportlayoutsservice_setdefaultreport)
