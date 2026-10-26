# TaxWebSiteParams — Parámetros de sitios web de impuestos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `TaxWebSiteParams`
- **Descripción (ES):** Parámetros de sitios web de impuestos
- **Description (EN):** Tax Web Site Parameters

- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` | Edm.Int32 | Yes | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `WebSiteName` | Edm.String | Yes | Web Site Name | Nombre del sitio web |

## Used by (service operations)

- [`TaxWebSitesService_GetDefaultWebSite`](../Servicios/TaxWebSitesService.md#taxwebsitesservice_getdefaultwebsite)
- [`TaxWebSitesService_GetTaxWebSiteList`](../Servicios/TaxWebSitesService.md#taxwebsitesservice_gettaxwebsitelist)
