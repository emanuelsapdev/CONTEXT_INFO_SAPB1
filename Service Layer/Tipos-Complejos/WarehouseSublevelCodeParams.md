# WarehouseSublevelCodeParams — Parámetros de códigos de subnivel de almacén

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `WarehouseSublevelCodeParams`
- **Descripción (ES):** Parámetros de códigos de subnivel de almacén
- **Description (EN):** Warehouse Sublevel Code Parameters

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` | Edm.Int32 | Yes | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `WarehouseSublevel` | Edm.Int32 | Yes | Warehouse Sublevel | Subnivel del almacén |
| 3 | `Code` | Edm.String | Yes | Code | Código |

## Used by (service operations)

- [`WarehouseSublevelCodesService_GetList`](../Servicios/WarehouseSublevelCodesService.md#warehousesublevelcodesservice_getlist)
