# ItemPrice — Precio del artículo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ItemPrice`
- **Descripción (ES):** Precio del artículo
- **Description (EN):** Item Price
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 10

## Properties (10)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `PriceList` | Edm.Int32 | Yes | Price List | Lista de precios |
| 2 | `Price` | Edm.Double | Yes | Price | Precio |
| 3 | `Currency` | Edm.String | Yes | Currency | Moneda |
| 4 | `AdditionalPrice1` | Edm.Double | Yes | Additional Price 1 | Precio adicional 1 |
| 5 | `AdditionalCurrency1` | Edm.String | Yes | Additional Currency 1 | Moneda adicional 1 |
| 6 | `AdditionalPrice2` | Edm.Double | Yes | Additional Price 2 | Precio adicional 2 |
| 7 | `AdditionalCurrency2` | Edm.String | Yes | Additional Currency 2 | Moneda adicional 2 |
| 8 | `BasePriceList` | Edm.Int32 | Yes | Base Price List | Lista de precios base |
| 9 | `Factor` | Edm.Double | Yes | Factor | Factor |
| 10 | `UoMPrices` | Collection([UoMPrice](../Tipos-Complejos/UoMPrice.md)) | Yes | Uo M Prices | Precios por unidad de medida |

## Used by (properties)

- [Item](../Entidades/Items.md).`ItemPrices`
