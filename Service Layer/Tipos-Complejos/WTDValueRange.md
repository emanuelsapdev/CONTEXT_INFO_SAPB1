# WTDValueRange — [Loc. AR] Rango de valores de la definición de retención

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `WTDValueRange`
- **Descripción (ES):** [Loc. AR] Rango de valores de la definición de retención
- **Description (EN):** WTD Value Range
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 5

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 2 | `SeqNum` | Edm.Int32 | Yes | Seq Number | Número de secuencia |
| 3 | `EffectiveFrom` | Edm.DateTimeOffset | Yes | Effective From | Vigente desde |
| 4 | `ValueFrom` | Edm.Double | Yes | Value From | Valor desde |
| 5 | `Rate` | Edm.Double | Yes | Rate | Tasa / tipo de cambio |

## Used by (properties)

- [WTDEffectiveDate](WTDEffectiveDate.md).`WTDValueRangeCollection`
