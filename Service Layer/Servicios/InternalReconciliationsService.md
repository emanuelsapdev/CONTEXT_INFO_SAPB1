# InternalReconciliationsService — Servicio de conciliaciones internas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `InternalReconciliationsService`
- **Descripción (ES):** Servicio de conciliaciones internas
- **Operations:** 2

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`InternalReconciliationsService_GetOpenTransactions`](#internalreconciliationsservice_getopentransactions) | action | [InternalReconciliationOpenTrans](../Tipos-Complejos/InternalReconciliationOpenTrans.md) | Get Open Transactions | Obtener transacciones abiertas |
| [`InternalReconciliationsService_RequestApproveCancellation`](#internalreconciliationsservice_requestapprovecancellation) | action | — | Request Approve Cancellation | Solicitar aprobación de cancelación |

## InternalReconciliationsService_GetOpenTransactions

- **Descripción (ES):** Obtener transacciones abiertas
- **Request:** `POST /b1s/v2/InternalReconciliationsService_GetOpenTransactions`
- **Parameters:** `InternalReconciliationOpenTransParams` ([InternalReconciliationOpenTransParams](../Tipos-Complejos/InternalReconciliationOpenTransParams.md))
- **Returns:** [InternalReconciliationOpenTrans](../Tipos-Complejos/InternalReconciliationOpenTrans.md)

```json
{
  "InternalReconciliationOpenTransParams": {
    "ReconDate": "2026-01-31",
    "AccountNo": "string",
    "FromDate": "2026-01-31",
    "ToDate": "2026-01-31",
    ...
  }
}
```

## InternalReconciliationsService_RequestApproveCancellation

- **Descripción (ES):** Solicitar aprobación de cancelación
- **Request:** `POST /b1s/v2/InternalReconciliationsService_RequestApproveCancellation`
- **Parameters:** `InternalReconciliation` ([InternalReconciliation](../Entidades/InternalReconciliations.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "InternalReconciliation": {
    "ReconNum": 0,
    "ReconDate": "2026-01-31",
    "Total": 0.0,
    "CancelAbs": 0,
    ...
  }
}
```

