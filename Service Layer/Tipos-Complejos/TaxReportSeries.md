# TaxReportSeries — Serie del informe de impuestos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `TaxReportSeries`
- **Descripción (ES):** Serie del informe de impuestos
- **Description (EN):** Tax Report Series

- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocumentType` | [TaxReportFilterDocumentType](../Enums/TaxReportFilterDocumentType.md) | Yes | Document Type | Tipo de documento |
| 2 | `SeriesCode` | Edm.Int32 | Yes | Series Code | Código de serie |

## Used by (properties)

- [TaxReportFilter](../Entidades/ReportFilter.md).`TaxReportSeriesCollection`
