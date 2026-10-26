# SalesTaxCodes_Line — Líneas de códigos del impuesto sobre ventas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `SalesTaxCodes_Line`
- **Descripción (ES):** Líneas de códigos del impuesto sobre ventas
- **Description (EN):** Sales Tax Codes Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 7

## Properties (7)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `STATaxOnTaxType` | Edm.Int32 | Yes | STA Tax On Tax Type | Tipo de impuesto sobre impuesto STA |
| 2 | `STATaxonTaxCode` | Edm.String | Yes | STA Taxon Tax Code | Código de impuesto sobre impuesto STA |
| 3 | `STCCode` | Edm.String | Yes | STC Code | Código STC |
| 4 | `STAType` | Edm.Int32 | Yes | STA Type | Tipo STA |
| 5 | `STACode` | Edm.String | Yes | STA Code | Código STA |
| 6 | `RowNumber` | Edm.Int32 | Yes | Row Number | Número de línea |
| 7 | `EffectiveRate` | Edm.Double | Yes | Effective Rate | Tasa efectiva |

## Used by (properties)

- [SalesTaxCode](../Entidades/SalesTaxCodes.md).`SalesTaxCodes_Lines`
