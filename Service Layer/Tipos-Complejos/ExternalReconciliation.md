# ExternalReconciliation — Conciliación externa

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ExternalReconciliation`
- **Descripción (ES):** Conciliación externa
- **Description (EN):** External Reconciliation

- **Properties:** 10

## Properties (10)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ReconciliationAccountType` | [ReconciliationAccountTypeEnum](../Enums/ReconciliationAccountTypeEnum.md) | Yes | Reconciliation Account Type | Tipo de cuenta de conciliación |
| 2 | `AccountCode` | Edm.String | Yes | Account Code | Código de cuenta |
| 3 | `ReconciliationNo` | Edm.Int32 | Yes | Reconciliation Number | Número de conciliación |
| 4 | `Amount` | Edm.Double | Yes | Amount | Importe |
| 5 | `CurrencyType` | Edm.String | Yes | Currency Type | Tipo de moneda |
| 6 | `ReconciliationType` | Edm.String | Yes | Reconciliation Type | Tipo de conciliación |
| 7 | `ReconciliationDate` | Edm.DateTimeOffset | Yes | Reconciliation Date | Fecha de conciliación |
| 8 | `CreationDate` | Edm.DateTimeOffset | Yes | Creation Date | Fecha de creación |
| 9 | `ReconciliationJournalEntryLines` | Collection([ReconciliationJournalEntryLine](../Tipos-Complejos/ReconciliationJournalEntryLine.md)) | Yes | Reconciliation Journal Entry Lines | Líneas de asiento de la conciliación |
| 10 | `ReconciliationBankStatementLines` | Collection([ReconciliationBankStatementLine](../Tipos-Complejos/ReconciliationBankStatementLine.md)) | Yes | Reconciliation Bank Statement Lines | Líneas de extracto bancario de la conciliación |

## Used by (service operations)

- [`ExternalReconciliationsService_GetReconciliation`](../Servicios/ExternalReconciliationsService.md#externalreconciliationsservice_getreconciliation)
- [`ExternalReconciliationsService_Reconcile`](../Servicios/ExternalReconciliationsService.md#externalreconciliationsservice_reconcile)
