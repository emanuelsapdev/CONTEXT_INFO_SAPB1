# ResourceWarehouse — Almacenes del recurso

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ResourceWarehouse`
- **Descripción (ES):** Almacenes del recurso
- **Description (EN):** Resource Warehouse
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` | Edm.String | Yes | Code | Código |
| 2 | `Warehouse` | Edm.String | Yes | Warehouse | Almacén |
| 3 | `Locked` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Locked | Bloqueado |

## Used by (properties)

- [Resource](../Entidades/Resources.md).`ResourceWarehouses`
