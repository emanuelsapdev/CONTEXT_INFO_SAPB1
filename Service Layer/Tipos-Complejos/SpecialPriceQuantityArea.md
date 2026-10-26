# SpecialPriceQuantityArea — Rangos de cantidades del precio especial

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `SpecialPriceQuantityArea`
- **Descripción (ES):** Rangos de cantidades del precio especial
- **Description (EN):** Special Price Quantity Area
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 9

## Properties (9)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Quantity` | Edm.Double | Yes | Quantity | Cantidad |
| 2 | `SPDARowNumber` | Edm.Int32 | Yes | SPDA Row Number | Línea SPDA |
| 3 | `SpecialPrice` | Edm.Double | Yes | Special Price | Precio especial |
| 4 | `ItemNo` | Edm.String | Yes | Item Number | Número de artículo |
| 5 | `BPCode` | Edm.String | Yes | Business Partner Code | Código del socio de negocios |
| 6 | `RowNumber` | Edm.Int32 | Yes | Row Number | Número de línea |
| 7 | `PriceCurrency` | Edm.String | Yes | Price Currency | Moneda del precio |
| 8 | `Discountin` | Edm.Double | Yes | Discountin | Descuento en |
| 9 | `UoMEntry` | Edm.Int32 | Yes | Uo M Entry | Entrada de unidad de medida (UomEntry) |

## Used by (properties)

- [SpecialPriceDataArea](SpecialPriceDataArea.md).`SpecialPriceQuantityAreas`
