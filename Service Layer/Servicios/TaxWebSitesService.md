# TaxWebSitesService — Servicio de sitios web de impuestos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `TaxWebSitesService`
- **Descripción (ES):** Servicio de sitios web de impuestos
- **Operations:** 2

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`TaxWebSitesService_GetDefaultWebSite`](#taxwebsitesservice_getdefaultwebsite) | action | [TaxWebSiteParams](../Tipos-Complejos/TaxWebSiteParams.md) | Get Default Web Site | Obtener sitio web predeterminado |
| [`TaxWebSitesService_GetTaxWebSiteList`](#taxwebsitesservice_gettaxwebsitelist) | action | Collection([TaxWebSiteParams](../Tipos-Complejos/TaxWebSiteParams.md)) | Get Tax Web Site List | Obtener lista de sitios web de impuestos |

## TaxWebSitesService_GetDefaultWebSite

- **Descripción (ES):** Obtener sitio web predeterminado
- **Request:** `POST /b1s/v2/TaxWebSitesService_GetDefaultWebSite`
- **Parameters:** none
- **Returns:** [TaxWebSiteParams](../Tipos-Complejos/TaxWebSiteParams.md)

## TaxWebSitesService_GetTaxWebSiteList

- **Descripción (ES):** Obtener lista de sitios web de impuestos
- **Request:** `POST /b1s/v2/TaxWebSitesService_GetTaxWebSiteList`
- **Parameters:** none
- **Returns:** Collection([TaxWebSiteParams](../Tipos-Complejos/TaxWebSiteParams.md))

