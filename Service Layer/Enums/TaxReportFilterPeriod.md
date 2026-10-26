# TaxReportFilterPeriod — Período del filtro de informe de impuestos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `TaxReportFilterPeriod`
- **Descripción (ES):** Período del filtro de informe de impuestos
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `trfP_Quarter` | 0 | Trf P Quarter | Trimestre |
| `trfP_Year` | 1 | Trf P Year | Año |
| `trfP_Month` | 2 | Trf P Month | Mes |
| `trfP_NULL` | 3 | Trf P NULL | Ninguno |

## Used by (1 properties)

- [TaxReportFilter](../Entidades/ReportFilter.md).`Period`
