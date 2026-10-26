# DocumentSeriesUserParams — Parámetros de series de documento por usuario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DocumentSeriesUserParams`
- **Descripción (ES):** Parámetros de series de documento por usuario
- **Description (EN):** Document Series User Parameters

- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Document` | Edm.String | Yes | Document | Documento |
| 2 | `DocumentSubType` | Edm.String | Yes | Document Sub Type | Subtipo de documento |
| 3 | `Series` | Edm.Int32 | Yes | Series | Serie de numeración |
| 4 | `User` | Edm.Int32 | Yes | User | Usuario |

## Used by (service operations)

- [`SeriesService_SetDefaultSeriesForUser`](../Servicios/SeriesService.md#seriesservice_setdefaultseriesforuser)
