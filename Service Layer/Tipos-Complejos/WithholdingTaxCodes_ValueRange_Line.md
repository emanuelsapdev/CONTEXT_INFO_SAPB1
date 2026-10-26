# WithholdingTaxCodes_ValueRange_Line — Líneas de rangos de valores de códigos de retención

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `WithholdingTaxCodes_ValueRange_Line`
- **Descripción (ES):** Líneas de rangos de valores de códigos de retención
- **Description (EN):** Withholding Tax Codes Value Range Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ValueFrom` | Edm.Double | Yes | Value From | Valor desde |
| 2 | `WTaxToBeDeductible` | Edm.Double | Yes | W Tax To Be Deductible | Retención a deducir |
| 3 | `Rate` | Edm.Double | Yes | Rate | Tasa / tipo de cambio |

## Used by (properties)

- [WithholdingTaxCodes_Line](WithholdingTaxCodes_Line.md).`WithholdingTaxCodes_ValueRange_Lines`
