# InventoryPostingCopyOption — Opción de copia a contabilización de inventario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `InventoryPostingCopyOption`
- **Descripción (ES):** Opción de copia a contabilización de inventario
- **Description (EN):** Inventory Posting Copy Option

- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `BaseEntry` | Edm.Int32 | Yes | Base Entry | Entrada base (DocEntry del documento base) |
| 2 | `CopyOption` | [InventoryPostingCopyOptionEnum](../Enums/InventoryPostingCopyOptionEnum.md) | Yes | Copy Option | Opción de copia |

## Used by (service operations)

- [`InventoryPostingsService_SetCopyOption`](../Servicios/InventoryPostingsService.md#inventorypostingsservice_setcopyoption)
