# BoDepositTypeEnum — Tipo de depósito

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoDepositTypeEnum`
- **Descripción (ES):** Tipo de depósito
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `dtChecks` | 0 | Checks | Cheques |
| `dtCredit` | 1 | Credit | Tarjetas de crédito |
| `dtCash` | 2 | Cash | Efectivo |
| `dtBOE` | 3 | BOE | Letras de cambio |

## Used by (1 properties)

- [Deposit](../Entidades/Deposits.md).`DepositType`
