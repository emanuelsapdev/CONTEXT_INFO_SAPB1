# RoutingDateCalculationService — Servicio de cálculo de fechas de ruta

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `RoutingDateCalculationService`
- **Descripción (ES):** Servicio de cálculo de fechas de ruta
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`RoutingDateCalculationService_Calculate`](#routingdatecalculationservice_calculate) | action | [RoutingDateCalculationOutput](../Tipos-Complejos/RoutingDateCalculationOutput.md) | Calculate | Calcular |

## RoutingDateCalculationService_Calculate

- **Descripción (ES):** Calcular
- **Request:** `POST /b1s/v2/RoutingDateCalculationService_Calculate`
- **Parameters:** `RoutingDateCalculationInput` ([RoutingDateCalculationInput](../Tipos-Complejos/RoutingDateCalculationInput.md))
- **Returns:** [RoutingDateCalculationOutput](../Tipos-Complejos/RoutingDateCalculationOutput.md)

```json
{
  "RoutingDateCalculationInput": {
    "ResourceCode": "string",
    "WarehouseCode": "string",
    "CalculateFromDate": "2026-01-31",
    "CalculateUntilDate": "2026-01-31",
    ...
  }
}
```

