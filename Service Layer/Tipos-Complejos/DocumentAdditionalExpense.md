# DocumentAdditionalExpense — Gastos adicionales del documento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DocumentAdditionalExpense`
- **Descripción (ES):** Gastos adicionales del documento
- **Description (EN):** Document Additional Expense
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 59

## Properties (59)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ExpenseCode` | Edm.Int32 | Yes | Expense Code | Código de gasto |
| 2 | `LineTotal` | Edm.Double | Yes | Line Total | Total de línea |
| 3 | `LineTotalFC` | Edm.Double | Yes | Line Total FC (foreign currency) | Total de línea (ME) |
| 4 | `LineTotalSys` | Edm.Double | Yes | Line Total (system currency) | Total de línea (moneda del sistema) |
| 5 | `PaidToDate` | Edm.Double | Yes | Paid To Date | Pagado hasta la fecha |
| 6 | `PaidToDateFC` | Edm.Double | Yes | Paid To Date FC (foreign currency) | Pagado hasta la fecha (ME) |
| 7 | `PaidToDateSys` | Edm.Double | Yes | Paid To Date (system currency) | Pagado hasta la fecha (moneda del sistema) |
| 8 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 9 | `DistributionMethod` | [BoAdEpnsDistribMethods](../Enums/BoAdEpnsDistribMethods.md) | Yes | Distribution Method | Método de distribución |
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
| 32 | `BaseDocEntry` | Edm.Int32 | Yes | Base Document Entry | DocEntry del documento base |
| 33 | `BaseDocLine` | Edm.Int32 | Yes | Base Document Line | Línea del documento base |
| 34 | `BaseDocType` | Edm.Int32 | Yes | Base Document Type | Tipo de documento base |
| 35 | `BaseDocumentReference` | Edm.Int32 | Yes | Base Document Reference | Referencia del documento base |
| 36 | `LineNum` | Edm.Int32 | Yes | Line Number | Número de línea |
| 37 | `LastPurchasePrice` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Last Purchase Price | Último precio de compra |
| 38 | `Status` | [BoStatus](../Enums/BoStatus.md) | Yes | Status | Estado |
| 39 | `Stock` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Stock | Stock |
| 40 | `TargetAbsEntry` | Edm.Int32 | Yes | Target Abs Entry | Entrada absoluta de destino |
| 41 | `TargetType` | Edm.Int32 | Yes | Target Type | Tipo de destino |
| 42 | `WTLiable` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Withholding Tax Liable | Sujeto a retención |
| 43 | `DistributionRule` | Edm.String | Yes | Distribution Rule | Norma de reparto |
| 44 | `Project` | Edm.String | Yes | Project | Proyecto |
| 45 | `DistributionRule2` | Edm.String | Yes | Distribution Rule 2 | Norma de reparto 2 |
| 46 | `DistributionRule3` | Edm.String | Yes | Distribution Rule 3 | Norma de reparto 3 |
| 47 | `DistributionRule4` | Edm.String | Yes | Distribution Rule 4 | Norma de reparto 4 |
| 48 | `DistributionRule5` | Edm.String | Yes | Distribution Rule 5 | Norma de reparto 5 |
| 49 | `LineGross` | Edm.Double | Yes | Line Gross | Bruto de línea |
| 50 | `LineGrossSys` | Edm.Double | Yes | Line Gross (system currency) | Bruto de línea (moneda del sistema) |
| 51 | `LineGrossFC` | Edm.Double | Yes | Line Gross FC (foreign currency) | Bruto de línea (ME) |
| 52 | `ExternalCalcTaxRate` | Edm.Double | Yes | External Calc Tax Rate | Tasa de impuesto calculada externamente |
| 53 | `ExternalCalcTaxAmount` | Edm.Double | Yes | External Calc Tax Amount | Importe de impuesto calculado externamente |
| 54 | `ExternalCalcTaxAmountFC` | Edm.Double | Yes | External Calc Tax Amount FC (foreign currency) | Importe de impuesto calculado externamente (ME) |
| 55 | `ExternalCalcTaxAmountSC` | Edm.Double | Yes | External Calc Tax Amount SC (system currency) | Importe de impuesto calculado externamente (moneda del sistema) |
| 56 | `CUSplit` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | CU Split | División CU |
| 57 | `DocFreight` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Document Freight | Gastos adicionales del documento |
| 58 | `DocExpenseTaxJurisdictions` | Collection([DocExpenseTaxJurisdiction](../Tipos-Complejos/DocExpenseTaxJurisdiction.md)) | Yes | Document Expense Tax Jurisdictions | Jurisdicciones fiscales de gastos del documento |
| 59 | `DocFreightEBooksDetails` | Collection([DocFreightEBooksDetail](../Tipos-Complejos/DocFreightEBooksDetail.md)) | Yes | Document Freight E Books Details | Detalles de libros electrónicos de gastos adicionales |

## Used by (properties)

- [Document](../Entidades/PurchaseQuotations.md).`DocumentAdditionalExpenses`
