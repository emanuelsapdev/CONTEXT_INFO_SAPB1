# TaxReportFilterType — Tipo de filtro de informe de impuestos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `TaxReportFilterType`
- **Descripción (ES):** Tipo de filtro de informe de impuestos
- **Underlying type:** Edm.Int32
- **Members:** 12

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `trft_TaxReport` | 0 | Tax Report | Informe de impuestos |
| `trft_WTReport` | 1 | Withholding Tax Report | Informe de retenciones |
| `trft_Report347` | 2 | Report 347 | Modelo 347 |
| `trft_Report349` | 3 | Report 349 | Modelo 349 |
| `trft_ReconciliationReport` | 4 | Reconciliation Report | Informe de conciliación |
| `trft_StampTax` | 5 | Stamp Tax | Impuesto de timbre |
| `trft_SalesReport` | 6 | Sales Report | Informe de ventas |
| `trft_None` | 7 | None | Ninguno |
| `trft_BoxReport` | 8 | Box Report | Informe de casillas |
| `trft_AppendixOP` | 9 | Appendix OP | Anexo O/P |
| `trft_AnnualSalesReport` | 10 | Annual Sales Report | Informe anual de ventas |
| `trft_VATRefundReport` | 11 | VAT Refund Report | Informe de devolución de IVA |

## Used by (2 properties)

- [TaxReportFilter](../Entidades/ReportFilter.md).`FilterType`
- [TaxReportFilterParams](../Tipos-Complejos/TaxReportFilterParams.md).`FilterType`
