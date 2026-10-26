# InventoryPostingCopyOptionEnum — Opción de copia a contabilización de inventario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `InventoryPostingCopyOptionEnum`
- **Descripción (ES):** Opción de copia a contabilización de inventario
- **Underlying type:** Edm.Int32
- **Members:** 7

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `ipcoNoCountersDiff` | 0 | Number Counters Diff | Sin diferencias entre contadores |
| `ipcoIndividual1CountedQuantity` | 1 | Individual 1 Counted Quantity | Cantidad contada por el contador individual 1 |
| `ipcoIndividual2CountedQuantity` | 2 | Individual 2 Counted Quantity | Cantidad contada por el contador individual 2 |
| `ipcoIndividual3CountedQuantity` | 3 | Individual 3 Counted Quantity | Cantidad contada por el contador individual 3 |
| `ipcoIndividual4CountedQuantity` | 4 | Individual 4 Counted Quantity | Cantidad contada por el contador individual 4 |
| `ipcoIndividual5CountedQuantity` | 5 | Individual 5 Counted Quantity | Cantidad contada por el contador individual 5 |
| `ipcoTeamCountedQuantity` | 6 | Team Counted Quantity | Cantidad contada por el equipo |

## Used by (1 properties)

- [InventoryPostingCopyOption](../Tipos-Complejos/InventoryPostingCopyOption.md).`CopyOption`
