# DeductionTaxHierarchies_Line — Líneas de la jerarquía de deducción de retenciones

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DeductionTaxHierarchies_Line`
- **Descripción (ES):** Líneas de la jerarquía de deducción de retenciones
- **Description (EN):** Deduction Tax Hierarchies Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `RowNumber` | Edm.Int32 | Yes | Row Number | Número de línea |
| 2 | `DeductionPercent` | Edm.Double | Yes | Deduction Percent | Porcentaje de deducción |
| 3 | `MaximumTotal` | Edm.Double | Yes | Maximum Total | Total máximo |

## Used by (properties)

- [DeductionTaxHierarchy](../Entidades/DeductionTaxHierarchies.md).`DeductionTaxHierarchies_Lines`
