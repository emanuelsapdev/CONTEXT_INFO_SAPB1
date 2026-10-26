# CampaignItem — Artículos de la campaña

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `CampaignItem`
- **Descripción (ES):** Artículos de la campaña
- **Description (EN):** Campaign Item
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 6

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `CampaignNumber` | Edm.Int32 | Yes | Campaign Number | Número de campaña |
| 2 | `CampaignLineNumber` | Edm.Int32 | Yes | Campaign Line Number | Número de línea de la campaña |
| 3 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |
| 4 | `ItemName` | Edm.String | Yes | Item Name | Nombre del artículo |
| 5 | `ItemType` | [CampaignItemTypeEnum](../Enums/CampaignItemTypeEnum.md) | Yes | Item Type | Tipo de artículo |
| 6 | `ItemGroup` | Edm.String | Yes | Item Group | Grupo de artículos |

## Used by (properties)

- [Campaign](../Entidades/Campaigns.md).`CampaignItems`
