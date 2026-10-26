# RclRecurringTransactionParams — Parámetros de transacción recurrente

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `RclRecurringTransactionParams`
- **Descripción (ES):** Parámetros de transacción recurrente
- **Description (EN):** Rcl Recurring Transaction Parameters

- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TransactionID` | Edm.Int32 | Yes | Transaction ID | ID de transacción |
| 2 | `PlannedDate` | Edm.DateTimeOffset | Yes | Planned Date | Fecha planificada |

## Used by (service operations)

- [`RecurringTransactionService_DeleteRecurringTransactions`](../Servicios/RecurringTransactionService.md#recurringtransactionservice_deleterecurringtransactions)
- [`RecurringTransactionService_ExecuteRecurringTransactions`](../Servicios/RecurringTransactionService.md#recurringtransactionservice_executerecurringtransactions)
- [`RecurringTransactionService_GetRecurringTransaction`](../Servicios/RecurringTransactionService.md#recurringtransactionservice_getrecurringtransaction)
