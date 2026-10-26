# ReconciliationJournalEntryLine — Líneas de asiento de la conciliación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ReconciliationJournalEntryLine`
- **Descripción (ES):** Líneas de asiento de la conciliación
- **Description (EN):** Reconciliation Journal Entry Line

- **Properties:** 10

## Properties (10)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TransactionNumber` | Edm.Int32 | Yes | Transaction Number | Número de transacción |
| 2 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `PostingDate` | Edm.DateTimeOffset | Yes | Posting Date | Fecha de contabilización |
| 4 | `DueDate` | Edm.DateTimeOffset | Yes | Due Date | Fecha de vencimiento |
| 5 | `Ref1` | Edm.String | Yes | Ref 1 | Referencia 1 |
| 6 | `Ref2` | Edm.String | Yes | Ref 2 | Referencia 2 |
| 7 | `Ref3` | Edm.String | Yes | Ref 3 | Referencia 3 |
| 8 | `DebitAmount` | Edm.Double | Yes | Debit Amount | Importe del debe |
| 9 | `CreditAmount` | Edm.Double | Yes | Credit Amount | Importe del haber |
| 10 | `Details` | Edm.String | Yes | Details | Detalles |

## Used by (properties)

- [ExternalReconciliation](ExternalReconciliation.md).`ReconciliationJournalEntryLines`
