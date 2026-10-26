# TaxReportGroup — Grupos del informe de impuestos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `TaxReportGroup`
- **Descripción (ES):** Grupos del informe de impuestos
- **Description (EN):** Tax Report Group

- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` | Edm.String | Yes | Code | Código |
| 2 | `Sum` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Sum | Importe |

## Used by (properties)

- [TaxReportFilter](../Entidades/ReportFilter.md).`TaxReportGroups`
