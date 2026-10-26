# ServiceTaxPostingService — Servicio de contabilización de impuestos de servicios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `ServiceTaxPostingService`
- **Descripción (ES):** Servicio de contabilización de impuestos de servicios
- **Operations:** 2

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`ServiceTaxPostingService_GetTaxableDeliveries`](#servicetaxpostingservice_gettaxabledeliveries) | action | Collection([ServiceTaxPostingParams](../Tipos-Complejos/ServiceTaxPostingParams.md)) | Get Taxable Deliveries | Obtener entregas imponibles |
| [`ServiceTaxPostingService_PostServiceTax`](#servicetaxpostingservice_postservicetax) | action | — | Post Service Tax | Contabilizar impuesto de servicios |

## ServiceTaxPostingService_GetTaxableDeliveries

- **Descripción (ES):** Obtener entregas imponibles
- **Request:** `POST /b1s/v2/ServiceTaxPostingService_GetTaxableDeliveries`
- **Parameters:** none
- **Returns:** Collection([ServiceTaxPostingParams](../Tipos-Complejos/ServiceTaxPostingParams.md))

## ServiceTaxPostingService_PostServiceTax

- **Descripción (ES):** Contabilizar impuesto de servicios
- **Request:** `POST /b1s/v2/ServiceTaxPostingService_PostServiceTax`
- **Parameters:** `ServiceTaxPostingParams` ([ServiceTaxPostingParams](../Tipos-Complejos/ServiceTaxPostingParams.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "ServiceTaxPostingParams": {
    "DocEntry": 0
  }
}
```

