# DocumentLineAdditionalExpense — Gastos adicionales de la línea del documento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DocumentLineAdditionalExpense`
- **Descripción (ES):** Gastos adicionales de la línea del documento
- **Description (EN):** Document Line Additional Expense
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 47

## Properties (47)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 2 | `GroupCode` | Edm.Int32 | Yes | Group Code | Código de grupo |
| 3 | `ExpenseCode` | Edm.Int32 | Yes | Expense Code | Código de gasto |
| 4 | `LineTotal` | Edm.Double | Yes | Line Total | Total de línea |
| 5 | `LineTotalFC` | Edm.Double | Yes | Line Total FC (foreign currency) | Total de línea (ME) |
| 6 | `LineTotalSys` | Edm.Double | Yes | Line Total (system currency) | Total de línea (moneda del sistema) |
| 7 | `PaidToDate` | Edm.Double | Yes | Paid To Date | Pagado hasta la fecha |
| 8 | `PaidToDateFC` | Edm.Double | Yes | Paid To Date FC (foreign currency) | Pagado hasta la fecha (ME) |
| 9 | `PaidToDateSys` | Edm.Double | Yes | Paid To Date (system currency) | Pagado hasta la fecha (moneda del sistema) |
| 10 | `TaxLiable` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Tax Liable | Sujeto a impuestos |
| 11 | `VatGroup` | Edm.String | Yes | Vat Group | Grupo de IVA (indicador de impuesto) |
| 12 | `TaxPercent` | Edm.Double | Yes | Tax Percent | Porcentaje de impuesto |
| 13 | `TaxSum` | Edm.Double | Yes | Tax Sum | Importe de impuestos |
| 14 | `TaxSumFC` | Edm.Double | Yes | Tax Sum FC (foreign currency) | Importe de impuestos (ME) |
| 15 | `TaxSumSys` | Edm.Double | Yes | Tax Sum (system currency) | Importe de impuestos (moneda del sistema) |
| 16 | `DeductibleTaxSum` | Edm.Double | Yes | Deductible Tax Sum | Importe de impuesto deducible |
| 17 | `DeductibleTaxSumFC` | Edm.Double | Yes | Deductible Tax Sum FC (foreign currency) | Importe de impuesto deducible (ME) |
| 18 | `DeductibleTaxSumSys` | Edm.Double | Yes | Deductible Tax Sum (system currency) | Importe de impuesto deducible (moneda del sistema) |
| 19 | `AquisitionTax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Aquisition Tax | Impuesto de adquisición |
| 20 | `TaxCode` | Edm.String | Yes | Tax Code | Indicador de impuesto |
| 21 | `TaxType` | [BoAdEpnsTaxTypes](../Enums/BoAdEpnsTaxTypes.md) | Yes | Tax Type | Tipo de impuesto |
| 22 | `TaxPaid` | Edm.Double | Yes | Tax Paid | Impuesto pagado |
| 23 | `TaxPaidFC` | Edm.Double | Yes | Tax Paid FC (foreign currency) | Impuesto pagado (ME) |
| 24 | `TaxPaidSys` | Edm.Double | Yes | Tax Paid (system currency) | Impuesto pagado (moneda del sistema) |
| 25 | `EqualizationTaxPercent` | Edm.Double | Yes | Equalization Tax Percent | Porcentaje de recargo de equivalencia |
| 26 | `EqualizationTaxSum` | Edm.Double | Yes | Equalization Tax Sum | Importe de recargo de equivalencia |
| 27 | `EqualizationTaxFC` | Edm.Double | Yes | Equalization Tax FC (foreign currency) | Recargo de equivalencia (ME) |
| 28 | `EqualizationTaxSys` | Edm.Double | Yes | Equalization Tax (system currency) | Recargo de equivalencia (moneda del sistema) |
| 29 | `TaxTotalSum` | Edm.Double | Yes | Tax Total Sum | Total de impuestos |
| 30 | `TaxTotalSumFC` | Edm.Double | Yes | Tax Total Sum FC (foreign currency) | Total de impuestos (ME) |
| 31 | `TaxTotalSumSys` | Edm.Double | Yes | Tax Total Sum (system currency) | Total de impuestos (moneda del sistema) |
| 32 | `WTLiable` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Withholding Tax Liable | Sujeto a retención |
| 33 | `BaseGroup` | Edm.Int32 | Yes | Base Group | Grupo base |
| 34 | `DistributionRule` | Edm.String | Yes | Distribution Rule | Norma de reparto |
| 35 | `Project` | Edm.String | Yes | Project | Proyecto |
| 36 | `DistributionRule2` | Edm.String | Yes | Distribution Rule 2 | Norma de reparto 2 |
| 37 | `DistributionRule3` | Edm.String | Yes | Distribution Rule 3 | Norma de reparto 3 |
| 38 | `DistributionRule4` | Edm.String | Yes | Distribution Rule 4 | Norma de reparto 4 |
| 39 | `DistributionRule5` | Edm.String | Yes | Distribution Rule 5 | Norma de reparto 5 |
| 40 | `ExternalCalcTaxRate` | Edm.Double | Yes | External Calc Tax Rate | Tasa de impuesto calculada externamente |
| 41 | `ExternalCalcTaxAmount` | Edm.Double | Yes | External Calc Tax Amount | Importe de impuesto calculado externamente |
| 42 | `ExternalCalcTaxAmountFC` | Edm.Double | Yes | External Calc Tax Amount FC (foreign currency) | Importe de impuesto calculado externamente (ME) |
| 43 | `ExternalCalcTaxAmountSC` | Edm.Double | Yes | External Calc Tax Amount SC (system currency) | Importe de impuesto calculado externamente (moneda del sistema) |
| 44 | `CUSplit` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | CU Split | División CU |
| 45 | `DocFreight` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Document Freight | Gastos adicionales del documento |
| 46 | `LineExpenseTaxJurisdictions` | Collection([LineExpenseTaxJurisdiction](../Tipos-Complejos/LineExpenseTaxJurisdiction.md)) | Yes | Line Expense Tax Jurisdictions | Jurisdicciones fiscales de gastos de línea |
| 47 | `LineFreightEBooksDetails` | Collection([LineFreightEBooksDetail](../Tipos-Complejos/LineFreightEBooksDetail.md)) | Yes | Line Freight E Books Details | Detalles de libros electrónicos de gastos de línea |

## Used by (properties)

- [DocumentLine](DocumentLine.md).`DocumentLineAdditionalExpenses`
