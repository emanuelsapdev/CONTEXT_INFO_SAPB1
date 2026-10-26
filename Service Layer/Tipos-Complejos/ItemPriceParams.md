# ItemPriceParams — Parámetros de precio del artículo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ItemPriceParams`
- **Descripción (ES):** Parámetros de precio del artículo
- **Description (EN):** Item Price Parameters

- **Properties:** 10

## Properties (10)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Date` | Edm.DateTimeOffset | Yes | Date | Fecha |
| 2 | `UoMEntry` | Edm.Int32 | Yes | Uo M Entry | Entrada de unidad de medida (UomEntry) |
| 3 | `BlanketAgreementNumber` | Edm.Int32 | Yes | Blanket Agreement Number | Número de acuerdo global |
| 4 | `BlanketAgreementLine` | Edm.Int32 | Yes | Blanket Agreement Line | Línea de acuerdo global |
| 5 | `UoMQuantity` | Edm.Double | Yes | Uo M Quantity | Cantidad en unidad de medida |
| 6 | `InventoryQuantity` | Edm.Double | Yes | Inventory Quantity | Cantidad de inventario |
| 7 | `Currency` | Edm.String | Yes | Currency | Moneda |
| 8 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |
| 9 | `CardCode` | Edm.String | Yes | Card Code | Código del socio de negocios |
| 10 | `PriceList` | Edm.Int32 | Yes | Price List | Lista de precios |

## Used by (service operations)

- [`CompanyService_GetItemPrice`](../Servicios/CompanyService.md#companyservice_getitemprice)
