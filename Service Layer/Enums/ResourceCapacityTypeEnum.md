# ResourceCapacityTypeEnum — Tipo de capacidad del recurso

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ResourceCapacityTypeEnum`
- **Descripción (ES):** Tipo de capacidad del recurso
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `rctInternal` | 0 | Internal | Interna |
| `rctOrdered` | 1 | Ordered | Pedida |
| `rctCommitted` | 2 | Committed | Comprometida |
| `rctConsumed` | 3 | Consumed | Consumida |

## Used by (3 properties)

- [ResourceCapacity](../Entidades/ResourceCapacities.md).`Type`
- [ResourceCapacityParams](../Tipos-Complejos/ResourceCapacityParams.md).`Type`
- [ResourceCapacityWithFilterParams](../Tipos-Complejos/ResourceCapacityWithFilterParams.md).`Type`
