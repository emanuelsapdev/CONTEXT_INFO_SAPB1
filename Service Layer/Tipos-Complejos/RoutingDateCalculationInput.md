# RoutingDateCalculationInput — Entrada del cálculo de fechas de ruta

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `RoutingDateCalculationInput`
- **Descripción (ES):** Entrada del cálculo de fechas de ruta
- **Description (EN):** Routing Date Calculation Input

- **Properties:** 9

## Properties (9)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ResourceCode` | Edm.String | Yes | Resource Code | Código de recurso |
| 2 | `WarehouseCode` | Edm.String | Yes | Warehouse Code | Código de almacén |
| 3 | `CalculateFromDate` | Edm.DateTimeOffset | Yes | Calculate From Date | Calcular desde fecha |
| 4 | `CalculateUntilDate` | Edm.DateTimeOffset | Yes | Calculate Until Date | Calcular hasta fecha |
| 5 | `CapacitySum` | Edm.Double | Yes | Capacity Sum | Capacidad total |
| 6 | `FirstDateProportion` | Edm.Double | Yes | First Date Proportion | Proporción de la primera fecha |
| 7 | `ResourceAlloc` | [ResourceAllocationEnum](../Enums/ResourceAllocationEnum.md) | Yes | Resource Alloc | Asignación de recursos |
| 8 | `WORObjAbs` | Edm.Int32 | Yes | WOR Obj Abs | Entrada de orden de fabricación |
| 9 | `WORLine` | Edm.Int32 | Yes | WOR Line | Línea de orden de fabricación |

## Used by (service operations)

- [`RoutingDateCalculationService_Calculate`](../Servicios/RoutingDateCalculationService.md#routingdatecalculationservice_calculate)
