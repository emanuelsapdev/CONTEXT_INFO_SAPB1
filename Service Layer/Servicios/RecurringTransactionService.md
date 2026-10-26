# RecurringTransactionService — Servicio de transacciones recurrentes

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `RecurringTransactionService`
- **Descripción (ES):** Servicio de transacciones recurrentes
- **Operations:** 4

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`RecurringTransactionService_DeleteRecurringTransactions`](#recurringtransactionservice_deleterecurringtransactions) | action | — | Delete Recurring Transactions | Eliminar transacciones recurrentes |
| [`RecurringTransactionService_ExecuteRecurringTransactions`](#recurringtransactionservice_executerecurringtransactions) | action | Collection([RclRecurringTransaction](../Tipos-Complejos/RclRecurringTransaction.md)) | Execute Recurring Transactions | Ejecutar transacciones recurrentes |
| [`RecurringTransactionService_GetAvailableRecurringTransactions`](#recurringtransactionservice_getavailablerecurringtransactions) | action | Collection([RclRecurringTransaction](../Tipos-Complejos/RclRecurringTransaction.md)) | Get Available Recurring Transactions | Obtener transacciones recurrentes disponibles |
| [`RecurringTransactionService_GetRecurringTransaction`](#recurringtransactionservice_getrecurringtransaction) | action | [RclRecurringTransaction](../Tipos-Complejos/RclRecurringTransaction.md) | Get Recurring Transaction | Obtener transacción recurrente |

## RecurringTransactionService_DeleteRecurringTransactions

- **Descripción (ES):** Eliminar transacciones recurrentes
- **Request:** `POST /b1s/v2/RecurringTransactionService_DeleteRecurringTransactions`
- **Parameters:** `RclRecurringTransactionParamsCollection` (Collection([RclRecurringTransactionParams](../Tipos-Complejos/RclRecurringTransactionParams.md)))
- **Returns:** nothing (`204 No Content`)

```json
{
  "RclRecurringTransactionParamsCollection": [ {
    "TransactionID": 0,
    "PlannedDate": "2026-01-31"
  } ]
}
```

## RecurringTransactionService_ExecuteRecurringTransactions

- **Descripción (ES):** Ejecutar transacciones recurrentes
- **Request:** `POST /b1s/v2/RecurringTransactionService_ExecuteRecurringTransactions`
- **Parameters:** `RclRecurringTransactionParamsCollection` (Collection([RclRecurringTransactionParams](../Tipos-Complejos/RclRecurringTransactionParams.md))), `RclRecurringExecutionParams` ([RclRecurringExecutionParams](../Tipos-Complejos/RclRecurringExecutionParams.md))
- **Returns:** Collection([RclRecurringTransaction](../Tipos-Complejos/RclRecurringTransaction.md))

```json
{
  "RclRecurringTransactionParamsCollection": [ {
    "TransactionID": 0,
    "PlannedDate": "2026-01-31"
  } ],
  "RclRecurringExecutionParams": { }
}
```

## RecurringTransactionService_GetAvailableRecurringTransactions

- **Descripción (ES):** Obtener transacciones recurrentes disponibles
- **Request:** `POST /b1s/v2/RecurringTransactionService_GetAvailableRecurringTransactions`
- **Parameters:** none
- **Returns:** Collection([RclRecurringTransaction](../Tipos-Complejos/RclRecurringTransaction.md))

## RecurringTransactionService_GetRecurringTransaction

- **Descripción (ES):** Obtener transacción recurrente
- **Request:** `POST /b1s/v2/RecurringTransactionService_GetRecurringTransaction`
- **Parameters:** `RclRecurringTransactionParams` ([RclRecurringTransactionParams](../Tipos-Complejos/RclRecurringTransactionParams.md))
- **Returns:** [RclRecurringTransaction](../Tipos-Complejos/RclRecurringTransaction.md)

```json
{
  "RclRecurringTransactionParams": {
    "TransactionID": 0,
    "PlannedDate": "2026-01-31"
  }
}
```

