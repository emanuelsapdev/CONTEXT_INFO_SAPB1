# ReconciliationBankStatementLine — Líneas de extracto bancario de la conciliación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ReconciliationBankStatementLine`
- **Descripción (ES):** Líneas de extracto bancario de la conciliación
- **Description (EN):** Reconciliation Bank Statement Line

- **Properties:** 6

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `BankStatementAccountCode` | Edm.String | Yes | Bank Statement Account Code | Código de cuenta del extracto bancario |
| 2 | `Sequence` | Edm.Int32 | Yes | Sequence | Secuencia |
| 3 | `Date` | Edm.DateTimeOffset | Yes | Date | Fecha |
| 4 | `Ref1` | Edm.String | Yes | Ref 1 | Referencia 1 |
| 5 | `Amount` | Edm.Double | Yes | Amount | Importe |
| 6 | `Details` | Edm.String | Yes | Details | Detalles |

## Used by (properties)

- [ExternalReconciliation](ExternalReconciliation.md).`ReconciliationBankStatementLines`
