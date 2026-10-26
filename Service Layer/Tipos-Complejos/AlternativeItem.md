# AlternativeItem — Artículos alternativos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `AlternativeItem`
- **Descripción (ES):** Artículos alternativos
- **Description (EN):** Alternative Item

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AlternativeItemCode` | Edm.String | Yes | Alternative Item Code | Código de artículo alternativo |
| 2 | `MatchFactor` | Edm.Double | Yes | Match Factor | Factor de coincidencia |
| 3 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |

## Used by (properties)

- [OriginalItem](OriginalItem.md).`AlternativeItems`
