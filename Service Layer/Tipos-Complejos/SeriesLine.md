# SeriesLine — Líneas de la serie

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `SeriesLine`
- **Descripción (ES):** Líneas de la serie
- **Description (EN):** Series Line

- **Properties:** 5

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Series` | Edm.Int32 | Yes | Series | Serie de numeración |
| 2 | `Prefix` | Edm.String | Yes | Prefix | Prefijo |
| 3 | `FirstNum` | Edm.Int32 | Yes | First Number | Primer número |
| 4 | `NextNum` | Edm.Int32 | Yes | Next Number | Siguiente número |
| 5 | `LastNum` | Edm.Int32 | Yes | Last Number | Último número |

## Used by (properties)

- [CertificateSeries](../Entidades/CertificateSeries.md).`SeriesLines`
