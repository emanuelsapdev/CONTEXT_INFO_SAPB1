# MultiplePayment — Pagos múltiples

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `MultiplePayment`
- **Descripción (ES):** Pagos múltiples
- **Description (EN):** Multiple Payment

- **Properties:** 6

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `BankStatmentLineID` | Edm.Int32 | Yes | Bank Statment Line ID | ID de línea del extracto bancario |
| 2 | `ListLineID` | Edm.Int32 | Yes | List Line ID | ID de línea de la lista |
| 3 | `DocumentIdentifier` | Edm.String | Yes | Document Identifier | Identificador del documento |
| 4 | `AmountLC` | Edm.Double | Yes | Amount LC (local currency) | Importe (moneda local) |
| 5 | `AmountFC` | Edm.Double | Yes | Amount FC (foreign currency) | Importe (ME) |
| 6 | `IsDebit` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Debit | Es débito |

## Used by (properties)

- [BankStatementRow](BankStatementRow.md).`MultiplePayments`
