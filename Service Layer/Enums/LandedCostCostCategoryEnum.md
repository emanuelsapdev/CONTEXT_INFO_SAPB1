# LandedCostCostCategoryEnum — Categoría de costo de importación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `LandedCostCostCategoryEnum`
- **Descripción (ES):** Categoría de costo de importación
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `lccc_CustomsVAT` | 0 | Customs VAT | IVA de aduana |
| `lccc_ExciseCost` | 1 | Excise Cost | Costo de impuestos especiales |
| `lccc_CustomsDuty` | 2 | Customs Duty | Derechos de aduana |

## Used by (1 properties)

- [LandedCost_CostLine](../Tipos-Complejos/LandedCost_CostLine.md).`CostCategory`
