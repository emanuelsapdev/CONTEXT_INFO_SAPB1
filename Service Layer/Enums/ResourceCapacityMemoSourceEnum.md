# ResourceCapacityMemoSourceEnum — Origen del comentario de capacidad

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ResourceCapacityMemoSourceEnum`
- **Descripción (ES):** Origen del comentario de capacidad
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `rcmsUnknown` | 0 | Unknown | Desconocido |
| `rcmsResourceCapacityForm` | 1 | Resource Capacity Form | Formulario de capacidad del recurso |
| `rcmsSetDailyInternalCapacitiesForm` | 2 | Set Daily Internal Capacities Form | Formulario de capacidades internas diarias |

## Used by (4 properties)

- [ResourceCapacity](../Entidades/ResourceCapacities.md).`MemoSource`
- [ResourceCapacity](../Entidades/ResourceCapacities.md).`SingleRunMemoSource`
- [ResourceCapacityParams](../Tipos-Complejos/ResourceCapacityParams.md).`MemoSource`
- [ResourceCapacityParams](../Tipos-Complejos/ResourceCapacityParams.md).`SingleRunMemoSource`
