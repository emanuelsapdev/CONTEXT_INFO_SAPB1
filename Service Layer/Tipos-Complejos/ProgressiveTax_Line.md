# ProgressiveTax_Line — Líneas de impuesto progresivo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ProgressiveTax_Line`
- **Descripción (ES):** Líneas de impuesto progresivo
- **Description (EN):** Progressive Tax Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TaxRate` | Edm.Double | Yes | Tax Rate | Tasa de impuesto |
| 2 | `MinAmount` | Edm.Double | Yes | Min Amount | Importe mínimo |
| 3 | `MaxAmount` | Edm.Double | Yes | Max Amount | Importe máximo |

## Used by (properties)

- [WithholdingTaxCodes_Line](WithholdingTaxCodes_Line.md).`ProgressiveTax_Lines`
