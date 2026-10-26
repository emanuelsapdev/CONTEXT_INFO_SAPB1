# ItemDistributionRule — Normas de reparto del artículo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ItemDistributionRule`
- **Descripción (ES):** Normas de reparto del artículo
- **Description (EN):** Item Distribution Rule

- **Properties:** 8

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 2 | `ValidFrom` | Edm.DateTimeOffset | Yes | Valid From | Válido desde |
| 3 | `ValidTo` | Edm.DateTimeOffset | Yes | Valid To | Válido hasta |
| 4 | `DistributionRule` | Edm.String | Yes | Distribution Rule | Norma de reparto |
| 5 | `DistributionRule2` | Edm.String | Yes | Distribution Rule 2 | Norma de reparto 2 |
| 6 | `DistributionRule3` | Edm.String | Yes | Distribution Rule 3 | Norma de reparto 3 |
| 7 | `DistributionRule4` | Edm.String | Yes | Distribution Rule 4 | Norma de reparto 4 |
| 8 | `DistributionRule5` | Edm.String | Yes | Distribution Rule 5 | Norma de reparto 5 |

## Used by (properties)

- [Item](../Entidades/Items.md).`ItemDistributionRules`
