# TrackingNoteItem — Artículo de la nota de seguimiento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `TrackingNoteItem`
- **Descripción (ES):** Artículo de la nota de seguimiento
- **Description (EN):** Tracking Note Item

- **Properties:** 10

## Properties (10)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TrackingNoteNumber` | Edm.Int32 | Yes | Tracking Note Number | Número de la nota de seguimiento |
| 2 | `TrackingNoteLineNumber` | Edm.Int32 | Yes | Tracking Note Line Number | Número de línea de la nota de seguimiento |
| 3 | `ItemCCDNumber` | Edm.String | Yes | Item CCD Number | Número de declaración aduanera del artículo |
| 4 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |
| 5 | `Quantity` | Edm.Double | Yes | Quantity | Cantidad |
| 6 | `CountryOfOrigin` | Edm.String | Yes | Country Of Origin | País de origen |
| 7 | `CustomsGroupCode` | Edm.Int32 | Yes | Customs Group Code | Código de grupo aduanero |
| 8 | `AccumulatedAPQuantity` | Edm.Double | Yes | Accumulated AP Quantity | Cantidad acumulada de compras |
| 9 | `AccumulatedARQuantity` | Edm.Double | Yes | Accumulated AR Quantity | Cantidad acumulada de ventas |
| 10 | `AccumulatedRelocatedQuantity` | Edm.Double | Yes | Accumulated Relocated Quantity | Cantidad reubicada acumulada |

## Used by (properties)

- [TrackingNote](../Entidades/TrackingNotes.md).`TrackingNoteItemCollection`
