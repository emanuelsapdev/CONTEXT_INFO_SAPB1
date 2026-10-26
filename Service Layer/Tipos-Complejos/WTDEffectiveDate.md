# WTDEffectiveDate — [Loc. AR] Fecha de vigencia de la definición de retención

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `WTDEffectiveDate`
- **Descripción (ES):** [Loc. AR] Fecha de vigencia de la definición de retención
- **Description (EN):** WTD Effective Date
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 8

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 2 | `EffectiveFrom` | Edm.DateTimeOffset | Yes | Effective From | Vigente desde |
| 3 | `Rate` | Edm.Double | Yes | Rate | Tasa / tipo de cambio |
| 4 | `U_B1SYS_Account` | Edm.String | Yes | [AR localization] Account | [Loc. AR] Cuenta contable |
| 5 | `U_B1SYS_FixedAmount` | Edm.Double | Yes | [AR localization] Fixed Amount | [Loc. AR] Importe fijo |
| 6 | `U_B1SYS_Currency` | Edm.String | Yes | [AR localization] Currency | [Loc. AR] Moneda |
| 7 | `U_B1SYS_NonDedAcc` | Edm.String | Yes | [AR localization] Non Ded Account | [Loc. AR] Cuenta no deducible |
| 8 | `WTDValueRangeCollection` | Collection([WTDValueRange](../Tipos-Complejos/WTDValueRange.md)) | Yes | WTD Value Range Collection | [Loc. AR] Colección de rangos de valores de la definición de retención |

## Used by (properties)

- [WTDCode](../Entidades/WitholdingTaxDefinition.md).`WTDEffectiveDateCollection`
