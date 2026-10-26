# BOEPortfolioParams — Parámetros de carteras de letras de cambio

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `BOEPortfolioParams`
- **Descripción (ES):** Parámetros de carteras de letras de cambio
- **Description (EN):** BOE Portfolio Parameters

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `PortfolioEntry` | Edm.Int32 | Yes | Portfolio Entry | Entrada de la cartera |
| 2 | `PortfolioID` | Edm.String | Yes | Portfolio ID | ID de cartera |
| 3 | `PortfolioCode` | Edm.String | Yes | Portfolio Code | Código de cartera |

## Used by (service operations)

- [`BOEPortfoliosService_GetBOEPortfolioList`](../Servicios/BOEPortfoliosService.md#boeportfoliosservice_getboeportfoliolist)
