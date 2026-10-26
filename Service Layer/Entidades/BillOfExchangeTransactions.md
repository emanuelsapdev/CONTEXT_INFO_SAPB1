# BillOfExchangeTransactions — Transacciones de letras de cambio

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `BillOfExchangeTransactions`
- **Descripción (ES):** Transacciones de letras de cambio
- **Entity type:** `BillOfExchangeTransaction` (open type: accepts dynamic/UDF properties)
- **Key:** `BOETransactionkey` (Edm.Int32)
- **DB tables (main / lines):** [OBOT](../../Tablas%20SAP%20B1/OBOT.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 12 · **Navigation properties:** 1 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/BillOfExchangeTransactions?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/BillOfExchangeTransactions/$count` | Contar |
| Get by key | `GET /b1s/v2/BillOfExchangeTransactions(1)` | Obtener por clave |
| Create | `POST /b1s/v2/BillOfExchangeTransactions` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/BillOfExchangeTransactions(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/BillOfExchangeTransactions(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/BillOfExchangeTransactions(1)` (only if the B1 object allows removal) | Borrar |

## Properties (12)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `StatusFrom` | [BoBOTFromStatus](../Enums/BoBOTFromStatus.md) | Yes | Status From | Estado desde |
| 2 | `StatusTo` | [BoBOTToStatus](../Enums/BoBOTToStatus.md) | Yes | Status To | Estado hasta |
| 3 | `TransactionDate` | Edm.DateTimeOffset | Yes | Transaction Date | Fecha de la transacción |
| 4 | `TransactionTime` | Edm.TimeOfDay | Yes | Transaction Time | Hora de la transacción |
| 5 | `IsBoeReconciled` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Boe Reconciled | Letra de cambio conciliada |
| 6 | `TransactionNumber` | Edm.Int32 | Yes | Transaction Number | Número de transacción |
| 7 | `PostingDate` | Edm.DateTimeOffset | Yes | Posting Date | Fecha de contabilización |
| 8 | `TaxDate` | Edm.DateTimeOffset | Yes | Tax Date | Fecha del documento (fecha de impuestos) |
| 9 | `BOETransactionkey` 🔑 | Edm.Int32 | No | BOE Transactionkey | Clave de transacción de letra de cambio |
| 10 | `BillOfExchangeTransactionLines` | Collection([BillOfExchangeTransactionLine](../Tipos-Complejos/BillOfExchangeTransactionLine.md)) | Yes | Bill Of Exchange Transaction Lines | Líneas de transacción de letras de cambio |
| 11 | `BillOfExchangeTransDeposits` | Collection([BillOfExchangeTransDeposit](../Tipos-Complejos/BillOfExchangeTransDeposit.md)) | Yes | Bill Of Exchange Trans Deposits | Depósitos de transacción de letras de cambio |
| 12 | `BillOfExchangeTransBankPages` | Collection([BillOfExchangeTransBankPage](../Tipos-Complejos/BillOfExchangeTransBankPage.md)) | Yes | Bill Of Exchange Trans Bank Pages | Páginas bancarias de transacción de letras de cambio |

## Navigation properties (1)

Use `GET /b1s/v2/BillOfExchangeTransactions(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `JournalEntry` | [JournalEntry](../Entidades/JournalEntries.md) | [JournalEntries](JournalEntries.md) | TransactionNumber → JdtNum | Asientos contables |
