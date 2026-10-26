# BoServicePaymentMethods — Método de pago de servicios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoServicePaymentMethods`
- **Descripción (ES):** Método de pago de servicios
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `spmAccreditedToBankAccount` | 0 | Accredited To Bank Account | Acreditado en cuenta bancaria |
| `spmBankTransfer` | 1 | Bank Transfer | Transferencia bancaria |
| `spmOther` | 2 | Other | Otro |

## Used by (1 properties)

- [ItemIntrastatExtension](../Tipos-Complejos/ItemIntrastatExtension.md).`ServicePaymentMethod`
