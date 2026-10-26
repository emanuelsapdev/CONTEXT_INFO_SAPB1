# TaxInvoiceReportLineTypeEnum — Tipo de línea del informe de facturas de impuestos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `TaxInvoiceReportLineTypeEnum`
- **Descripción (ES):** Tipo de línea del informe de facturas de impuestos
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `LineOfBusinessPlace` | 1 | Line Of Business Place | Línea de lugar de negocios |
| `LineOfBusinessPartner` | 2 | Line Of Business Partner | Línea de socio de negocios |
| `LineOfDocument` | 3 | Line Of Document | Línea de documento |
| `LineOfItem` | 4 | Line Of Item | Línea de artículo |

## Used by (1 properties)

- [TaxInvoiceReportLine](../Tipos-Complejos/TaxInvoiceReportLine.md).`LineType`
