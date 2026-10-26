# CampaignResponseTypeParams — Parámetros de tipos de respuesta de campaña

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `CampaignResponseTypeParams`
- **Descripción (ES):** Parámetros de tipos de respuesta de campaña
- **Description (EN):** Campaign Response Type Parameters

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ResponseType` | Edm.String | Yes | Response Type | Tipo de respuesta |
| 2 | `ResponseTypeDescription` | Edm.String | Yes | Response Type Description | Descripción del tipo de respuesta |
| 3 | `IsActive` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Active | Está activo |

## Used by (service operations)

- [`CampaignResponseTypeService_GetResponseTypeList`](../Servicios/CampaignResponseTypeService.md#campaignresponsetypeservice_getresponsetypelist)
