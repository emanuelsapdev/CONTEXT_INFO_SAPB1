# ResourceCapacityWithFilterParams — Parámetros de capacidad de recursos con filtro

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ResourceCapacityWithFilterParams`
- **Descripción (ES):** Parámetros de capacidad de recursos con filtro
- **Description (EN):** Resource Capacity With Filter Parameters

- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` | Edm.String | Yes | Code | Código |
| 2 | `Warehouse` | Edm.String | Yes | Warehouse | Almacén |
| 3 | `Date` | Edm.DateTimeOffset | Yes | Date | Fecha |
| 4 | `Type` | [ResourceCapacityTypeEnum](../Enums/ResourceCapacityTypeEnum.md) | Yes | Type | Tipo |

## Used by (service operations)

- [`ResourceCapacitiesService_GetListWithFilter`](../Servicios/ResourceCapacitiesService.md#resourcecapacitiesservice_getlistwithfilter)
