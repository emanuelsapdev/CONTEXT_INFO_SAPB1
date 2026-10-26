# ItemPriceReturnParams — Retorno de precio del artículo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ItemPriceReturnParams`
- **Descripción (ES):** Retorno de precio del artículo
- **Description (EN):** Item Price Return Parameters

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Price` | Edm.Double | Yes | Price | Precio |
| 2 | `Currency` | Edm.String | Yes | Currency | Moneda |
| 3 | `Discount` | Edm.Double | Yes | Discount | Descuento |

## Used by (service operations)

- [`CompanyService_GetItemPrice`](../Servicios/CompanyService.md#companyservice_getitemprice)
