# PartnersSetupParams — Parámetros de configuración de socios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `PartnersSetupParams`
- **Descripción (ES):** Parámetros de configuración de socios
- **Description (EN):** Partners Setup Parameters

- **Properties:** 5

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `PartnerID` | Edm.Int32 | Yes | Partner ID | ID del socio |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `DefaultRelationship` | Edm.Int32 | Yes | Default Relationship | Relación predeterminada |
| 4 | `RelatedBP` | Edm.String | Yes | Related Business Partner | Socio de negocios relacionado |
| 5 | `Details` | Edm.String | Yes | Details | Detalles |

## Used by (service operations)

- [`PartnersSetupsService_GetList`](../Servicios/PartnersSetupsService.md#partnerssetupsservice_getlist)
