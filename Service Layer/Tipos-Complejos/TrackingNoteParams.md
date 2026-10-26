# TrackingNoteParams — Parámetros de notas de seguimiento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `TrackingNoteParams`
- **Descripción (ES):** Parámetros de notas de seguimiento
- **Description (EN):** Tracking Note Parameters

- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TrackingNoteNumber` | Edm.Int32 | Yes | Tracking Note Number | Número de la nota de seguimiento |
| 2 | `CCDNumber` | Edm.String | Yes | CCD Number | Número de declaración aduanera de carga |

## Used by (service operations)

- [`TrackingNotesService_GetList`](../Servicios/TrackingNotesService.md#trackingnotesservice_getlist)
