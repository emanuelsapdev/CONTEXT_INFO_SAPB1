# ItemGroupsWarehouseInfo — Información de almacenes del grupo de artículos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ItemGroupsWarehouseInfo`
- **Descripción (ES):** Información de almacenes del grupo de artículos
- **Description (EN):** Item Groups Warehouse Information

- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ItmsGrpCod` | Edm.Int32 | Yes | Itms Group Cod | Código de grupo de artículos |
| 2 | `WarehouseCode` | Edm.String | Yes | Warehouse Code | Código de almacén |
| 3 | `DefaultBin` | Edm.Int32 | Yes | Default Bin | Ubicación predeterminada |
| 4 | `DefaultBinEnforced` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Default Bin Enforced | Ubicación predeterminada obligatoria |

## Used by (properties)

- [ItemGroups](../Entidades/ItemGroups.md).`ItemGroupsWarehouseInfos`
