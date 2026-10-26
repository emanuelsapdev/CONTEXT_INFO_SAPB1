# BoDepositCheckEnum — Depósito de cheques

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoDepositCheckEnum`
- **Descripción (ES):** Depósito de cheques
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `dtNo` | 0 | Number | No |
| `dcAsCash` | 1 | As Cash | Como efectivo |
| `dtAsPostdated` | 2 | As Postdated | Como diferido |

## Used by (1 properties)

- [CheckLine](../Tipos-Complejos/CheckLine.md).`Deposited`
