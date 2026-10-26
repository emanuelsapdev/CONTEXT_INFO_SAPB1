# DunningTermLine — Líneas de la condición de reclamación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DunningTermLine`
- **Descripción (ES):** Líneas de la condición de reclamación
- **Description (EN):** Dunning Term Line

- **Properties:** 8

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LevelNum` | Edm.Int32 | Yes | Level Number | Número de nivel |
| 2 | `LetterFormat` | [DunningLetterTypeEnum](../Enums/DunningLetterTypeEnum.md) | Yes | Letter Format | Formato de carta |
| 3 | `Effectiveafter` | Edm.String | Yes | Effectiveafter | Vigente después de |
| 4 | `LetterFee` | Edm.Double | Yes | Letter Fee | Cargo por carta |
| 5 | `LetterFeeCurrency` | Edm.String | Yes | Letter Fee Currency | Moneda del cargo por carta |
| 6 | `MininumBalance` | Edm.Double | Yes | Mininum Balance | Saldo mínimo |
| 7 | `MininumBalanceCurrency` | Edm.String | Yes | Mininum Balance Currency | Moneda del saldo mínimo |
| 8 | `CalculateInterest` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Calculate Interest | Calcular intereses |

## Used by (properties)

- [DunningTerm](../Entidades/DunningTerms.md).`DunningTermLines`
