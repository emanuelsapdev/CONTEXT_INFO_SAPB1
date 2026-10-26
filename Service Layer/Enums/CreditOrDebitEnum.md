# CreditOrDebitEnum — Haber o debe

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `CreditOrDebitEnum`
- **Descripción (ES):** Haber o debe
- **Underlying type:** Edm.Int32
- **Members:** 2

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `codCredit` | 0 | Credit | Haber |
| `codDebit` | 1 | Debit | Debe |

## Used by (2 properties)

- [InternalReconciliationOpenTransRow](../Tipos-Complejos/InternalReconciliationOpenTransRow.md).`CreditOrDebit`
- [InternalReconciliationRow](../Tipos-Complejos/InternalReconciliationRow.md).`CreditOrDebit`
