# ElectronicSeries — Serie electrónica

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ElectronicSeries`
- **Descripción (ES):** Serie electrónica
- **Description (EN):** Electronic Series

- **Properties:** 10

## Properties (10)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ElectronicSeriesProperty` | Edm.Int32 | Yes | Electronic Series Property | Propiedad de serie electrónica |
| 2 | `Series` | Edm.Int32 | Yes | Series | Serie de numeración |
| 3 | `Name` | Edm.String | Yes | Name | Nombre |
| 4 | `InitialNumber` | Edm.String | Yes | Initial Number | Número inicial |
| 5 | `NextNumber` | Edm.String | Yes | Next Number | Siguiente número |
| 6 | `LastNumber` | Edm.String | Yes | Last Number | Último número |
| 7 | `Prefix` | Edm.String | Yes | Prefix | Prefijo |
| 8 | `ApprovalYear` | Edm.Int32 | Yes | Approval Year | Año de autorización |
| 9 | `ApprovalNumber` | Edm.Int32 | Yes | Approval Number | Número de autorización |
| 10 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |

## Used by (service operations)

- [`SeriesService_AddElectronicSeries`](../Servicios/SeriesService.md#seriesservice_addelectronicseries)
- [`SeriesService_GetElectronicSeries`](../Servicios/SeriesService.md#seriesservice_getelectronicseries)
- [`SeriesService_UpdateElectronicSeries`](../Servicios/SeriesService.md#seriesservice_updateelectronicseries)
