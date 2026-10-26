# PostingMethodEnum — Método de contabilización (extracto bancario)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `PostingMethodEnum`
- **Descripción (ES):** Método de contabilización (extracto bancario)
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `pmGLAccountBankAccount` | 0 | G/L Account Bank Account | Cuenta de mayor - cuenta bancaria |
| `pmBussinessPartnerBankAccount` | 1 | Bussiness Partner Bank Account | Socio de negocios - cuenta bancaria |
| `pmInterimAccountBankAccount` | 2 | Interim Account Bank Account | Cuenta transitoria - cuenta bancaria |
| `pmExternalReconciliation` | 3 | External Reconciliation | Conciliación externa |
| `pmIgnore` | 4 | Ignore | Ignorar |

## Used by (1 properties)

- [BankStatementRow](../Tipos-Complejos/BankStatementRow.md).`PostingMethod`
