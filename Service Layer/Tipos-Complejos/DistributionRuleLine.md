# DistributionRuleLine — Líneas de la norma de reparto

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DistributionRuleLine`
- **Descripción (ES):** Líneas de la norma de reparto
- **Description (EN):** Distribution Rule Line

- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `CenterCode` | Edm.String | Yes | Center Code | Código del centro |
| 2 | `TotalInCenter` | Edm.Double | Yes | Total In Center | Total en el centro |
| 3 | `EffectiveFrom` | Edm.DateTimeOffset | Yes | Effective From | Vigente desde |
| 4 | `EffectiveTo` | Edm.DateTimeOffset | Yes | Effective To | Vigente hasta |

## Used by (properties)

- [DistributionRule](../Entidades/DistributionRules.md).`DistributionRuleLines`
