# SpecialPriceDataArea — Rangos de fechas del precio especial

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `SpecialPriceDataArea`
- **Descripción (ES):** Rangos de fechas del precio especial
- **Description (EN):** Special Price Data Area
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 11

## Properties (11)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `PriceCurrency` | Edm.String | Yes | Price Currency | Moneda del precio |
| 2 | `AutoUpdate` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Auto Update | Actualización automática |
| 3 | `Dateto` | Edm.DateTimeOffset | Yes | Dateto | Fecha hasta |
| 4 | `Discount` | Edm.Double | Yes | Discount | Descuento |
| 5 | `SpecialPrice` | Edm.Double | Yes | Special Price | Precio especial |
| 6 | `DateFrom` | Edm.DateTimeOffset | Yes | Date From | Fecha desde |
| 7 | `BPCode` | Edm.String | Yes | Business Partner Code | Código del socio de negocios |
| 8 | `PriceListNo` | Edm.Int32 | Yes | Price List Number | Número de lista de precios |
| 9 | `ItemNo` | Edm.String | Yes | Item Number | Número de artículo |
| 10 | `RowNumber` | Edm.Int32 | Yes | Row Number | Número de línea |
| 11 | `SpecialPriceQuantityAreas` | Collection([SpecialPriceQuantityArea](../Tipos-Complejos/SpecialPriceQuantityArea.md)) | Yes | Special Price Quantity Areas | Rangos de cantidades del precio especial |

## Used by (properties)

- [SpecialPrice](../Entidades/SpecialPrices.md).`SpecialPriceDataAreas`
