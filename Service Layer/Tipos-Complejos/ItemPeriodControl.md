# ItemPeriodControl — Control de períodos del artículo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ItemPeriodControl`
- **Descripción (ES):** Control de períodos del artículo
- **Description (EN):** Item Period Control

- **Properties:** 6

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `FiscalYear` | Edm.String | Yes | Fiscal Year | Ejercicio fiscal |
| 2 | `DepreciationArea` | Edm.String | Yes | Depreciation Area | Área de amortización |
| 3 | `SubPeriod` | Edm.Int32 | Yes | Sub Period | Subperíodo |
| 4 | `DepreciationStatus` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Depreciation Status | Estado de amortización |
| 5 | `Factor` | Edm.Double | Yes | Factor | Factor |
| 6 | `ActualUnits` | Edm.Int32 | Yes | Actual Units | Unidades reales |

## Used by (properties)

- [Item](../Entidades/Items.md).`ItemPeriodControls`
