# DocumentSeriesParams — Parámetros de series de documento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DocumentSeriesParams`
- **Descripción (ES):** Parámetros de series de documento
- **Description (EN):** Document Series Parameters

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Document` | Edm.String | Yes | Document | Documento |
| 2 | `DocumentSubType` | Edm.String | Yes | Document Sub Type | Subtipo de documento |
| 3 | `Series` | Edm.Int32 | Yes | Series | Serie de numeración |

## Used by (service operations)

- [`SeriesService_AttachSeriesToDocument`](../Servicios/SeriesService.md#seriesservice_attachseriestodocument)
- [`SeriesService_SetDefaultSeriesForAllUsers`](../Servicios/SeriesService.md#seriesservice_setdefaultseriesforallusers)
- [`SeriesService_SetDefaultSeriesForCurrentUser`](../Servicios/SeriesService.md#seriesservice_setdefaultseriesforcurrentuser)
- [`SeriesService_UnattachSeriesFromDocument`](../Servicios/SeriesService.md#seriesservice_unattachseriesfromdocument)
