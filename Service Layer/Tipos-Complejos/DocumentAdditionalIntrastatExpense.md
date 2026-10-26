# DocumentAdditionalIntrastatExpense — Gastos Intrastat adicionales del documento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DocumentAdditionalIntrastatExpense`
- **Descripción (ES):** Gastos Intrastat adicionales del documento
- **Description (EN):** Document Additional Intrastat Expense
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 13

## Properties (13)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ExpenseCode` | Edm.Int32 | Yes | Expense Code | Código de gasto |
| 2 | `LineTotal` | Edm.Double | Yes | Line Total | Total de línea |
| 3 | `LineTotalFC` | Edm.Double | Yes | Line Total FC (foreign currency) | Total de línea (ME) |
| 4 | `LineTotalSys` | Edm.Double | Yes | Line Total (system currency) | Total de línea (moneda del sistema) |
| 5 | `PaidToDate` | Edm.Double | Yes | Paid To Date | Pagado hasta la fecha |
| 6 | `PaidToDateFC` | Edm.Double | Yes | Paid To Date FC (foreign currency) | Pagado hasta la fecha (ME) |
| 7 | `PaidToDateSys` | Edm.Double | Yes | Paid To Date (system currency) | Pagado hasta la fecha (moneda del sistema) |
| 8 | `DistributionMethod` | [BoAdEpnsDistribMethods](../Enums/BoAdEpnsDistribMethods.md) | Yes | Distribution Method | Método de distribución |
| 9 | `BaseDocEntry` | Edm.Int32 | Yes | Base Document Entry | DocEntry del documento base |
| 10 | `BaseDocLine` | Edm.Int32 | Yes | Base Document Line | Línea del documento base |
| 11 | `BaseDocType` | Edm.Int32 | Yes | Base Document Type | Tipo de documento base |
| 12 | `BaseDocumentReference` | Edm.Int32 | Yes | Base Document Reference | Referencia del documento base |
| 13 | `LineNum` | Edm.Int32 | Yes | Line Number | Número de línea |

## Used by (properties)

- [Document](../Entidades/PurchaseQuotations.md).`DocumentAdditionalIntrastatExpenses`
