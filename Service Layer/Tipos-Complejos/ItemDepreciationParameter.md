# ItemDepreciationParameter — Parámetros de amortización del artículo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ItemDepreciationParameter`
- **Descripción (ES):** Parámetros de amortización del artículo
- **Description (EN):** Item Depreciation Parameter

- **Properties:** 10

## Properties (10)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `FiscalYear` | Edm.String | Yes | Fiscal Year | Ejercicio fiscal |
| 2 | `DepreciationArea` | Edm.String | Yes | Depreciation Area | Área de amortización |
| 3 | `DepreciationStartDate` | Edm.DateTimeOffset | Yes | Depreciation Start Date | Fecha de inicio de amortización |
| 4 | `DepreciationEndDate` | Edm.DateTimeOffset | Yes | Depreciation End Date | Fecha de fin de amortización |
| 5 | `UsefulLife` | Edm.Int32 | Yes | Useful Life | Vida útil |
| 6 | `RemainingLife` | Edm.Double | Yes | Remaining Life | Vida útil restante |
| 7 | `DepreciationType` | Edm.String | Yes | Depreciation Type | Tipo de amortización |
| 8 | `TotalUnitsInUsefulLife` | Edm.Int32 | Yes | Total Units In Useful Life | Unidades totales en la vida útil |
| 9 | `RemainingUnits` | Edm.Int32 | Yes | Remaining Units | Unidades restantes |
| 10 | `StandardUnits` | Edm.Int32 | Yes | Standard Units | Unidades estándar |

## Used by (properties)

- [Item](../Entidades/Items.md).`ItemDepreciationParameters`
