# WebClientVariantSortBy — Ordenamiento de la variante

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `WebClientVariantSortBy`
- **Descripción (ES):** Ordenamiento de la variante
- **Description (EN):** Web Client Variant Sort By

- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Guid` | Edm.String | Yes | Guid | GUID |
| 2 | `Order` | Edm.Int32 | Yes | Order | Pedido / orden |
| 3 | `ColumnName` | Edm.String | Yes | Column Name | Nombre de columna |
| 4 | `Direction` | Edm.String | Yes | Direction | Dirección (sentido) |

## Used by (properties)

- [WebClientVariant](../Entidades/WebClientVariants.md).`WebClientVariantSortByCollection`
