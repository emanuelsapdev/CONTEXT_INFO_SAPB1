# ResourceAllocationEnum — Asignación de recursos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ResourceAllocationEnum`
- **Descripción (ES):** Asignación de recursos
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `raOnStartDate` | 0 | On Start Date | En la fecha de inicio |
| `raOnEndDate` | 1 | On End Date | En la fecha de fin |
| `raStartDateForwards` | 2 | Start Date Forwards | Desde la fecha de inicio hacia adelante |
| `raEndDateBackwards` | 3 | End Date Backwards | Desde la fecha de fin hacia atrás |

## Used by (4 properties)

- [ProductionOrder](../Entidades/ProductionOrders.md).`RoutingDateCalculation`
- [ProductionOrderLine](../Tipos-Complejos/ProductionOrderLine.md).`ResourceAllocation`
- [Resource](../Entidades/Resources.md).`Allocation`
- [RoutingDateCalculationInput](../Tipos-Complejos/RoutingDateCalculationInput.md).`ResourceAlloc`
