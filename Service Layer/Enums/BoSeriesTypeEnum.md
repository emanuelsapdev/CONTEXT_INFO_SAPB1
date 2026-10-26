# BoSeriesTypeEnum — Tipo de serie

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoSeriesTypeEnum`
- **Descripción (ES):** Tipo de serie
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `stDocument` | 0 | Document | Documento |
| `stBusinessPartner` | 1 | Business Partner | Socio de negocios |
| `stItem` | 2 | Item | Artículo |
| `stResource` | 3 | Resource | Recurso |

## Used by (1 properties)

- [Series](../Tipos-Complejos/Series.md).`SeriesType`
