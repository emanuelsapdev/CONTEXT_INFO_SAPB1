# CampaignPartner — Socios de la campaña

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `CampaignPartner`
- **Descripción (ES):** Socios de la campaña
- **Description (EN):** Campaign Partner
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 6

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `CampaignNumber` | Edm.Int32 | Yes | Campaign Number | Número de campaña |
| 2 | `CampaignLineNumber` | Edm.Int32 | Yes | Campaign Line Number | Número de línea de la campaña |
| 3 | `PartnerID` | Edm.Int32 | Yes | Partner ID | ID del socio |
| 4 | `RelationshipCode` | Edm.Int32 | Yes | Relationship Code | Código de relación |
| 5 | `RelatedBP` | Edm.String | Yes | Related Business Partner | Socio de negocios relacionado |
| 6 | `Details` | Edm.String | Yes | Details | Detalles |

## Used by (properties)

- [Campaign](../Entidades/Campaigns.md).`CampaignPartners`
