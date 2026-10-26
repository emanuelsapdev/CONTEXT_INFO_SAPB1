# WithholdingTaxCodes_Line — Líneas de códigos de retención

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `WithholdingTaxCodes_Line`
- **Descripción (ES):** Líneas de códigos de retención
- **Description (EN):** Withholding Tax Codes Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 20

## Properties (20)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Effectivefrom` | Edm.DateTimeOffset | Yes | Effectivefrom | Vigente desde |
| 2 | `Rate` | Edm.Double | Yes | Rate | Tasa / tipo de cambio |
| 3 | `TDSRate` | Edm.Double | Yes | TDS Rate | Tasa TDS |
| 4 | `SurchargeRate` | Edm.Double | Yes | Surcharge Rate | Tasa de recargo |
| 5 | `CessRate` | Edm.Double | Yes | Cess Rate | Tasa de Cess |
| 6 | `HSCRate` | Edm.Double | Yes | HSC Rate | Tasa HSC |
| 7 | `IGSTRate` | Edm.Double | Yes | IGST Rate | Tasa IGST |
| 8 | `CGSTRate` | Edm.Double | Yes | CGST Rate | Tasa CGST |
| 9 | `SGSTRate` | Edm.Double | Yes | SGST Rate | Tasa SGST |
| 10 | `UTGSTRate` | Edm.Double | Yes | UTGST Rate | Tasa UTGST |
| 11 | `CessGSTRate` | Edm.Double | Yes | Cess GST Rate | Tasa de Cess GST |
| 12 | `LineNum` | Edm.Int32 | Yes | Line Number | Número de línea |
| 13 | `UoMEntry` | Edm.Int32 | Yes | Uo M Entry | Entrada de unidad de medida (UomEntry) |
| 14 | `UoMCode` | Edm.String | Yes | Uo M Code | Código de unidad de medida |
| 15 | `FixedAmount` | Edm.Double | Yes | Fixed Amount | Importe fijo |
| 16 | `Currency` | Edm.String | Yes | Currency | Moneda |
| 17 | `ITRNonCompliantRate` | Edm.Double | Yes | ITR Non Compliant Rate | Tasa por incumplimiento de ITR (India) |
| 18 | `PANNonCompliantRate` | Edm.Double | Yes | PAN Non Compliant Rate | Tasa por incumplimiento de PAN (India) |
| 19 | `ProgressiveTax_Lines` | Collection([ProgressiveTax_Line](../Tipos-Complejos/ProgressiveTax_Line.md)) | Yes | Progressive Tax Lines | Líneas de impuesto progresivo |
| 20 | `WithholdingTaxCodes_ValueRange_Lines` | Collection([WithholdingTaxCodes_ValueRange_Line](../Tipos-Complejos/WithholdingTaxCodes_ValueRange_Line.md)) | Yes | Withholding Tax Codes Value Range Lines | Líneas de rangos de valores de códigos de retención |

## Used by (properties)

- [WithholdingTaxCode](../Entidades/WithholdingTaxCodes.md).`WithholdingTaxCodes_Lines`
