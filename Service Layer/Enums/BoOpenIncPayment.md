# BoOpenIncPayment — Abrir pago recibido al agregar

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoOpenIncPayment`
- **Descripción (ES):** Abrir pago recibido al agregar
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `oip_No` | 0 | Number | No |
| `oip_Cash` | 1 | Cash | Efectivo |
| `oip_Checks` | 2 | Checks | Cheques |
| `oip_Credit` | 3 | Credit | Tarjeta de crédito |
| `oip_BankTransfer` | 4 | Bank Transfer | Transferencia bancaria |

## Used by (1 properties)

- [PaymentTermsType](../Entidades/PaymentTermsTypes.md).`OpenReceipt`
