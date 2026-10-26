# TransactionCodes — Códigos de transacción

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `TransactionCodes`
- **Descripción (ES):** Códigos de transacción
- **Entity type:** `TransactionCode`
- **Key:** `Code` (Edm.String)
- **DB tables (main / lines):** [OTRC](../../Tablas%20SAP%20B1/OTRC.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 2 · **Navigation properties:** 5 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/TransactionCodes?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/TransactionCodes/$count` | Contar |
| Get by key | `GET /b1s/v2/TransactionCodes('value')` | Obtener por clave |
| Create | `POST /b1s/v2/TransactionCodes` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/TransactionCodes('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/TransactionCodes('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/TransactionCodes('value')` (only if the B1 object allows removal) | Borrar |

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.String | No | Code | Código |
| 2 | `Description` | Edm.String | Yes | Description | Descripción |

## Navigation properties (5)

Use `GET /b1s/v2/TransactionCodes('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `VendorPayments` | Collection([Payment](../Entidades/VendorPayments.md)) | [VendorPayments](VendorPayments.md) |  | Pagos efectuados |
| `JournalEntries` | Collection([JournalEntry](../Entidades/JournalEntries.md)) | [JournalEntries](JournalEntries.md) |  | Asientos contables |
| `ChartOfAccounts` | Collection([ChartOfAccount](../Entidades/ChartOfAccounts.md)) | [ChartOfAccounts](ChartOfAccounts.md) |  | Plan de cuentas (cuentas de mayor) |
| `PaymentDrafts` | Collection([Payment](../Entidades/VendorPayments.md)) | [PaymentDrafts](PaymentDrafts.md) |  | Borradores de pagos |
| `IncomingPayments` | Collection([Payment](../Entidades/VendorPayments.md)) | [IncomingPayments](IncomingPayments.md) |  | Pagos recibidos |
