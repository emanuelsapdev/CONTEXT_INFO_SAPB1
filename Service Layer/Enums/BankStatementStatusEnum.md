# BankStatementStatusEnum — Estado del extracto bancario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BankStatementStatusEnum`
- **Descripción (ES):** Estado del extracto bancario
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `bssExecuted` | 0 | Executed | Ejecutado |
| `bssDraft` | 1 | Draft | Borrador |
| `bssOld` | 2 | Old | Antiguo |

## Used by (2 properties)

- [BankStatement](../Entidades/BankStatements.md).`Status`
- [BankStatementParams](../Tipos-Complejos/BankStatementParams.md).`Status`
