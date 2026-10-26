# ResourceCapacityActionEnum — Acción de capacidad del recurso

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ResourceCapacityActionEnum`
- **Descripción (ES):** Acción de capacidad del recurso
- **Underlying type:** Edm.Int32
- **Members:** 9

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `rcaUnknown` | 0 | Unknown | Desconocida |
| `rcaProductionOrderCreate` | 1 | Production Order Create | Crear orden de fabricación |
| `rcaProductionOrderClose` | 2 | Production Order Close | Cerrar orden de fabricación |
| `rcaProductionOrderReschedule` | 3 | Production Order Reschedule | Reprogramar orden de fabricación |
| `rcaProductionOrderAddLine` | 4 | Production Order Add Line | Agregar línea a la orden de fabricación |
| `rcaProductionOrderDeleteLine` | 5 | Production Order Delete Line | Eliminar línea de la orden de fabricación |
| `rcaProductionOrderUpdateLine` | 6 | Production Order Update Line | Actualizar línea de la orden de fabricación |
| `rcaIssueForProductionCreate` | 7 | Issue For Production Create | Crear emisión para producción |
| `rcaReceiptFromProductionCreate` | 8 | Receipt From Production Create | Crear recibo de producción |

## Used by (2 properties)

- [ResourceCapacity](../Entidades/ResourceCapacities.md).`Action`
- [ResourceCapacityParams](../Tipos-Complejos/ResourceCapacityParams.md).`Action`
