# TaxReportFilterParams — Parámetros de filtro de informes de impuestos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `TaxReportFilterParams`
- **Descripción (ES):** Parámetros de filtro de informes de impuestos
- **Description (EN):** Tax Report Filter Parameters

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` | Edm.Int32 | Yes | Code | Código |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `FilterType` | [TaxReportFilterType](../Enums/TaxReportFilterType.md) | Yes | Filter Type | Tipo de filtro |

## Used by (service operations)

- [`ReportFilterService_GetTaxReportFilterList`](../Servicios/ReportFilterService.md#reportfilterservice_gettaxreportfilterlist)
