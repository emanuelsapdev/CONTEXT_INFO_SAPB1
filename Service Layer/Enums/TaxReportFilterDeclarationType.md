# TaxReportFilterDeclarationType — Tipo de declaración del filtro de informe de impuestos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `TaxReportFilterDeclarationType`
- **Descripción (ES):** Tipo de declaración del filtro de informe de impuestos
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `trfdt_Original` | 0 | Original | Original |
| `trfdt_Substitute` | 1 | Substitute | Sustitutiva |
| `trfdt_Complementary` | 2 | Complementary | Complementaria |

## Used by (1 properties)

- [TaxReportFilter](../Entidades/ReportFilter.md).`DeclarationType`
