# BoUpdateAllocationEnum — Actualización de asignación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoUpdateAllocationEnum`
- **Descripción (ES):** Actualización de asignación
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `bouaManual` | 0 | Manual | Manual |
| `bouaCalculated` | 1 | Calculated | Calculada |
| `bouaRunCalculation` | 2 | Run Calculation | Ejecutar cálculo |

## Used by (1 properties)

- [ProductionOrder](../Entidades/ProductionOrders.md).`UpdateAllocation`
