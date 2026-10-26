# BoBpsDocTypes — Tipo de documento BPS

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoBpsDocTypes`
- **Descripción (ES):** Tipo de documento BPS
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `bpdt_PaymentReference` | 0 | Payment Reference | Referencia de pago |
| `bpdt_ISR` | 1 | ISR | ISR |
| `bpdt_DocNum` | 2 | Document Number | Número de documento |

## Used by (2 properties)

- [BankPage](../Entidades/BankPages.md).`DocNumberType`
- [BankStatementRow](../Tipos-Complejos/BankStatementRow.md).`DocNumType`
