# RclRecurringTransaction — Transacción recurrente

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `RclRecurringTransaction`
- **Descripción (ES):** Transacción recurrente
- **Description (EN):** Rcl Recurring Transaction

- **Properties:** 7

## Properties (7)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TransactionID` | Edm.Int32 | Yes | Transaction ID | ID de transacción |
| 2 | `TemplateID` | Edm.Int32 | Yes | Template ID | ID de plantilla |
| 3 | `Instance` | Edm.Int32 | Yes | Instance | Instancia |
| 4 | `PlannedDate` | Edm.DateTimeOffset | Yes | Planned Date | Fecha planificada |
| 5 | `Status` | [RclRecurringTransactionStatusEnum](../Enums/RclRecurringTransactionStatusEnum.md) | Yes | Status | Estado |
| 6 | `DocType` | Edm.String | Yes | Document Type | Tipo de documento (artículos/servicios) |
| 7 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |

## Used by (service operations)

- [`RecurringTransactionService_ExecuteRecurringTransactions`](../Servicios/RecurringTransactionService.md#recurringtransactionservice_executerecurringtransactions)
- [`RecurringTransactionService_GetAvailableRecurringTransactions`](../Servicios/RecurringTransactionService.md#recurringtransactionservice_getavailablerecurringtransactions)
- [`RecurringTransactionService_GetRecurringTransaction`](../Servicios/RecurringTransactionService.md#recurringtransactionservice_getrecurringtransaction)
