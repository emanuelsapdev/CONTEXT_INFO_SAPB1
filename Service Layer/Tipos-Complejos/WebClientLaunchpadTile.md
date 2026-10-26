# WebClientLaunchpadTile — Mosaicos del launchpad del cliente web

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `WebClientLaunchpadTile`
- **Descripción (ES):** Mosaicos del launchpad del cliente web
- **Description (EN):** Web Client Launchpad Tile

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Guid` | Edm.String | Yes | Guid | GUID |
| 2 | `Order` | Edm.Int32 | Yes | Order | Pedido / orden |
| 3 | `TileId` | Edm.String | Yes | Tile ID | ID de mosaico |

## Used by (properties)

- [WebClientLaunchpadGroup](WebClientLaunchpadGroup.md).`WebClientLaunchpadTiles`
