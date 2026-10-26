# UoMPrice — Precios por unidad de medida

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `UoMPrice`
- **Descripción (ES):** Precios por unidad de medida
- **Description (EN):** Uo M Price
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 12

## Properties (12)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `PriceList` | Edm.Int32 | Yes | Price List | Lista de precios |
| 2 | `UoMEntry` | Edm.Int32 | Yes | Uo M Entry | Entrada de unidad de medida (UomEntry) |
| 3 | `ReduceBy` | Edm.Double | Yes | Reduce By | Reducir en |
| 4 | `Price` | Edm.Double | Yes | Price | Precio |
| 5 | `Currency` | Edm.String | Yes | Currency | Moneda |
| 6 | `AdditionalReduceBy1` | Edm.Double | Yes | Additional Reduce By 1 | Reducción adicional 1 |
| 7 | `AdditionalPrice1` | Edm.Double | Yes | Additional Price 1 | Precio adicional 1 |
| 8 | `AdditionalCurrency1` | Edm.String | Yes | Additional Currency 1 | Moneda adicional 1 |
| 9 | `AdditionalReduceBy2` | Edm.Double | Yes | Additional Reduce By 2 | Reducción adicional 2 |
| 10 | `AdditionalPrice2` | Edm.Double | Yes | Additional Price 2 | Precio adicional 2 |
| 11 | `AdditionalCurrency2` | Edm.String | Yes | Additional Currency 2 | Moneda adicional 2 |
| 12 | `Auto` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Auto | Automático |

## Used by (properties)

- [ItemPrice](ItemPrice.md).`UoMPrices`
