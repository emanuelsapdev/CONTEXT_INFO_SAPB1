# ExternalReconciliationsService — Servicio de conciliaciones externas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `ExternalReconciliationsService`
- **Descripción (ES):** Servicio de conciliaciones externas
- **Operations:** 4

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`ExternalReconciliationsService_CancelReconciliation`](#externalreconciliationsservice_cancelreconciliation) | action | — | Cancel Reconciliation | Cancelar conciliación |
| [`ExternalReconciliationsService_GetReconciliation`](#externalreconciliationsservice_getreconciliation) | action | [ExternalReconciliation](../Tipos-Complejos/ExternalReconciliation.md) | Get Reconciliation | Obtener conciliación |
| [`ExternalReconciliationsService_GetReconciliationList`](#externalreconciliationsservice_getreconciliationlist) | action | Collection([ExternalReconciliationParams](../Tipos-Complejos/ExternalReconciliationParams.md)) | Get Reconciliation List | Obtener lista de conciliaciones |
| [`ExternalReconciliationsService_Reconcile`](#externalreconciliationsservice_reconcile) | action | — | Reconcile | Conciliar |

## ExternalReconciliationsService_CancelReconciliation

- **Descripción (ES):** Cancelar conciliación
- **Request:** `POST /b1s/v2/ExternalReconciliationsService_CancelReconciliation`
- **Parameters:** `ExternalReconciliationParams` ([ExternalReconciliationParams](../Tipos-Complejos/ExternalReconciliationParams.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "ExternalReconciliationParams": {
    "AccountCode": "string",
    "ReconciliationNo": 0
  }
}
```

## ExternalReconciliationsService_GetReconciliation

- **Descripción (ES):** Obtener conciliación
- **Request:** `POST /b1s/v2/ExternalReconciliationsService_GetReconciliation`
- **Parameters:** `ExternalReconciliationParams` ([ExternalReconciliationParams](../Tipos-Complejos/ExternalReconciliationParams.md))
- **Returns:** [ExternalReconciliation](../Tipos-Complejos/ExternalReconciliation.md)

```json
{
  "ExternalReconciliationParams": {
    "AccountCode": "string",
    "ReconciliationNo": 0
  }
}
```

## ExternalReconciliationsService_GetReconciliationList

- **Descripción (ES):** Obtener lista de conciliaciones
- **Request:** `POST /b1s/v2/ExternalReconciliationsService_GetReconciliationList`
- **Parameters:** `ExternalReconciliationFilterParams` ([ExternalReconciliationFilterParams](../Tipos-Complejos/ExternalReconciliationFilterParams.md))
- **Returns:** Collection([ExternalReconciliationParams](../Tipos-Complejos/ExternalReconciliationParams.md))

```json
{
  "ExternalReconciliationFilterParams": {
    "AccountCodeFrom": "string",
    "AccountCodeTo": "string",
    "ReconciliationDateFrom": "2026-01-31",
    "ReconciliationDateTo": "2026-01-31",
    ...
  }
}
```

## ExternalReconciliationsService_Reconcile

- **Descripción (ES):** Conciliar
- **Request:** `POST /b1s/v2/ExternalReconciliationsService_Reconcile`
- **Parameters:** `ExternalReconciliation` ([ExternalReconciliation](../Tipos-Complejos/ExternalReconciliation.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "ExternalReconciliation": {
    "AccountCode": "string",
    "ReconciliationNo": 0,
    "Amount": 0.0,
    "CurrencyType": "string",
    ...
  }
}
```

