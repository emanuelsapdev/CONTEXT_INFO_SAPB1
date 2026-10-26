# DepreciationLevel — Nivel de amortización

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DepreciationLevel`
- **Descripción (ES):** Nivel de amortización
- **Description (EN):** Depreciation Level

- **Properties:** 5

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Level` | Edm.Int32 | Yes | Level | Nivel |
| 2 | `DepreciationCalculationBase` | [DepreciationCalculationBaseEnum](../Enums/DepreciationCalculationBaseEnum.md) | Yes | Depreciation Calculation Base | Base de cálculo de amortización |
| 3 | `NumberOfYears` | Edm.Int32 | Yes | Number Of Years | Cantidad de años |
| 4 | `Percentage` | Edm.Double | Yes | Percentage | Porcentaje |
| 5 | `Amount` | Edm.Double | Yes | Amount | Importe |

## Used by (properties)

- [DepreciationType](../Entidades/DepreciationTypes.md).`DepreciationLevelCollection`
