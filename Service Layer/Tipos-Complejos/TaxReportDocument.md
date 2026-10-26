# TaxReportDocument — Documentos del informe de impuestos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `TaxReportDocument`
- **Descripción (ES):** Documentos del informe de impuestos
- **Description (EN):** Tax Report Document

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocumentType` | [TaxReportFilterDocumentType](../Enums/TaxReportFilterDocumentType.md) | Yes | Document Type | Tipo de documento |
| 2 | `FromNumber` | Edm.Int32 | Yes | From Number | Número desde |
| 3 | `ToNumber` | Edm.Int32 | Yes | To Number | Número hasta |

## Used by (properties)

- [TaxReportFilter](../Entidades/ReportFilter.md).`TaxReportDocuments`
