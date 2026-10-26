# WebClientLaunchpadGroup — Grupos del launchpad del cliente web

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `WebClientLaunchpadGroup`
- **Descripción (ES):** Grupos del launchpad del cliente web
- **Description (EN):** Web Client Launchpad Group

- **Properties:** 6

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Guid` | Edm.String | Yes | Guid | GUID |
| 2 | `Order` | Edm.Int32 | Yes | Order | Pedido / orden |
| 3 | `GroupId` | Edm.String | Yes | Group ID | ID de grupo |
| 4 | `GroupName` | Edm.String | Yes | Group Name | Nombre del grupo |
| 5 | `Visible` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Visible | Visible |
| 6 | `WebClientLaunchpadTiles` | Collection([WebClientLaunchpadTile](../Tipos-Complejos/WebClientLaunchpadTile.md)) | Yes | Web Client Launchpad Tiles | Mosaicos del launchpad del cliente web |

## Used by (properties)

- [WebClientLaunchpad](../Entidades/WebClientLaunchpads.md).`WebClientLaunchpadGroups`
