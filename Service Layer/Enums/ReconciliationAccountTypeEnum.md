# ReconciliationAccountTypeEnum — Tipo de cuenta de conciliación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ReconciliationAccountTypeEnum`
- **Descripción (ES):** Tipo de cuenta de conciliación
- **Underlying type:** Edm.Int32
- **Members:** 2

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `rat_GLAccount` | 0 | G/L Account | Cuenta de mayor |
| `rat_BusinessPartner` | 1 | Business Partner | Socio de negocios |

## Used by (2 properties)

- [ExternalReconciliation](../Tipos-Complejos/ExternalReconciliation.md).`ReconciliationAccountType`
- [ExternalReconciliationFilterParams](../Tipos-Complejos/ExternalReconciliationFilterParams.md).`ReconciliationAccountType`
