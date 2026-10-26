# MobileAppReportChoiceEnum — Selección de informe de la app móvil

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `MobileAppReportChoiceEnum`
- **Descripción (ES):** Selección de informe de la app móvil
- **Underlying type:** Edm.Int32
- **Members:** 2

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `marSystemReport` | 0 | System Report | Informe del sistema |
| `marCustomizedReport` | 1 | Customized Report | Informe personalizado |

## Used by (2 properties)

- [ServiceAppReport](../Tipos-Complejos/ServiceAppReport.md).`ReportChoice`
- [ServiceAppReportParams](../Tipos-Complejos/ServiceAppReportParams.md).`ReportChoice`
