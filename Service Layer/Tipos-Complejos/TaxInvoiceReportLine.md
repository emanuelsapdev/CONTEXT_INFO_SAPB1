# TaxInvoiceReportLine — Línea del informe de facturas de impuestos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `TaxInvoiceReportLine`
- **Descripción (ES):** Línea del informe de facturas de impuestos
- **Description (EN):** Tax Invoice Report Line

- **Properties:** 18

## Properties (18)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocumentType` | Edm.Int32 | Yes | Document Type | Tipo de documento |
| 2 | `DocumentEntry` | Edm.Int32 | Yes | Document Entry | Entrada del documento |
| 3 | `LineType` | [TaxInvoiceReportLineTypeEnum](../Enums/TaxInvoiceReportLineTypeEnum.md) | Yes | Line Type | Tipo de línea |
| 4 | `BaseAmount` | Edm.Double | Yes | Base Amount | Importe base |
| 5 | `TaxAmount` | Edm.Double | Yes | Tax Amount | Importe de impuestos |
| 6 | `ItemQuantity` | Edm.Double | Yes | Item Quantity | Cantidad del artículo |
| 7 | `ItemNo` | Edm.String | Yes | Item Number | Número de artículo |
| 8 | `ItemDescription` | Edm.String | Yes | Item Description | Descripción del artículo |
| 9 | `TaxCode` | Edm.String | Yes | Tax Code | Indicador de impuesto |
| 10 | `DocumentDate` | Edm.DateTimeOffset | Yes | Document Date | Fecha del documento |
| 11 | `ItemPrice` | Edm.Double | Yes | Item Price | Precio del artículo |
| 12 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 13 | `Currency` | Edm.String | Yes | Currency | Moneda |
| 14 | `BusinessPlace` | Edm.Int32 | Yes | Business Place | Lugar de negocios |
| 15 | `TaxInvoiceReportNumber` | Edm.String | Yes | Tax Invoice Report Number | Número del informe de facturas de impuestos |
| 16 | `BPCode` | Edm.String | Yes | Business Partner Code | Código del socio de negocios |
| 17 | `BPName` | Edm.String | Yes | Business Partner Name | Nombre del socio de negocios |
| 18 | `Legacy` | Edm.String | Yes | Legacy | Heredado |

## Used by (properties)

- [TaxInvoiceReport](../Entidades/TaxInvoiceReport.md).`TaxInvoiceReportLineCollection`
