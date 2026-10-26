# ReportFilterService — Servicio de filtros de informes de impuestos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `ReportFilterService`
- **Descripción (ES):** Servicio de filtros de informes de impuestos
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`ReportFilterService_GetTaxReportFilterList`](#reportfilterservice_gettaxreportfilterlist) | action | Collection([TaxReportFilterParams](../Tipos-Complejos/TaxReportFilterParams.md)) | Get Tax Report Filter List | Obtener lista de filtros de informes de impuestos |

## ReportFilterService_GetTaxReportFilterList

- **Descripción (ES):** Obtener lista de filtros de informes de impuestos
- **Request:** `POST /b1s/v2/ReportFilterService_GetTaxReportFilterList`
- **Parameters:** `TaxReportFilterParams` ([TaxReportFilterParams](../Tipos-Complejos/TaxReportFilterParams.md))
- **Returns:** Collection([TaxReportFilterParams](../Tipos-Complejos/TaxReportFilterParams.md))

```json
{
  "TaxReportFilterParams": {
    "Code": 0,
    "Name": "string",
    ...
  }
}
```

