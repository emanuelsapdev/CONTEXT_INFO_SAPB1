# CheckInParams — Parámetros de check-in

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `CheckInParams`
- **Descripción (ES):** Parámetros de check-in
- **Description (EN):** Check In Parameters

- **Properties:** 8

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 2 | `Date` | Edm.DateTimeOffset | Yes | Date | Fecha |
| 3 | `Time` | Edm.TimeOfDay | Yes | Time | Hora |
| 4 | `Location` | Edm.String | Yes | Location | Ubicación |
| 5 | `Latitude` | Edm.String | Yes | Latitude | Latitud |
| 6 | `Longitude` | Edm.String | Yes | Longitude | Longitud geográfica |
| 7 | `HandledBy` | Edm.Int32 | Yes | Handled By | Gestionado por |
| 8 | `HandledByEmployee` | Edm.Int32 | Yes | Handled By Employee | Gestionado por empleado |

## Used by (properties)

- [Activity](../Entidades/Activities.md).`CheckInListParams`
