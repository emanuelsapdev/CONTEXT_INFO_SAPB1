# LandedCostAllocationByEnum — Asignación de costos de importación por

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `LandedCostAllocationByEnum`
- **Descripción (ES):** Asignación de costos de importación por
- **Underlying type:** Edm.Int32
- **Members:** 7

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `asCashValueBeforeCustoms` | 0 | Cash Value Before Customs | Valor en efectivo antes de aduana |
| `asCashValueAfterCustoms` | 1 | Cash Value After Customs | Valor en efectivo después de aduana |
| `asQuantity` | 2 | Quantity | Cantidad |
| `asWeight` | 3 | Weight | Peso |
| `asVolume` | 4 | Volume | Volumen |
| `asEqual` | 5 | Equal | Partes iguales |
| `asLegalCost` | 6 | Legal Cost | Costo legal |

## Used by (1 properties)

- [LandedCost_CostLine](../Tipos-Complejos/LandedCost_CostLine.md).`AllocationBy`
