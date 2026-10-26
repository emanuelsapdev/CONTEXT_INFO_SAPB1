# DocExpenseTaxJurisdiction — Jurisdicciones fiscales de gastos del documento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DocExpenseTaxJurisdiction`
- **Descripción (ES):** Jurisdicciones fiscales de gastos del documento
- **Description (EN):** Document Expense Tax Jurisdiction
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 13

## Properties (13)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `JurisdictionCode` | Edm.String | Yes | Jurisdiction Code | Código de jurisdicción |
| 2 | `JurisdictionType` | Edm.Int32 | Yes | Jurisdiction Type | Tipo de jurisdicción |
| 3 | `TaxAmount` | Edm.Double | Yes | Tax Amount | Importe de impuestos |
| 4 | `TaxAmountSC` | Edm.Double | Yes | Tax Amount SC (system currency) | Importe de impuestos (moneda del sistema) |
| 5 | `TaxAmountFC` | Edm.Double | Yes | Tax Amount FC (foreign currency) | Importe de impuestos (ME) |
| 6 | `TaxRate` | Edm.Double | Yes | Tax Rate | Tasa de impuesto |
| 7 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 8 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 9 | `RowSequence` | Edm.Int32 | Yes | Row Sequence | Secuencia de línea |
| 10 | `ExternalCalcTaxRate` | Edm.Double | Yes | External Calc Tax Rate | Tasa de impuesto calculada externamente |
| 11 | `ExternalCalcTaxAmount` | Edm.Double | Yes | External Calc Tax Amount | Importe de impuesto calculado externamente |
| 12 | `ExternalCalcTaxAmountFC` | Edm.Double | Yes | External Calc Tax Amount FC (foreign currency) | Importe de impuesto calculado externamente (ME) |
| 13 | `ExternalCalcTaxAmountSC` | Edm.Double | Yes | External Calc Tax Amount SC (system currency) | Importe de impuesto calculado externamente (moneda del sistema) |

## Used by (properties)

- [DocumentAdditionalExpense](DocumentAdditionalExpense.md).`DocExpenseTaxJurisdictions`
