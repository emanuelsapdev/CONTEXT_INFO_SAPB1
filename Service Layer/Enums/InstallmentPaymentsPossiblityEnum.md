# InstallmentPaymentsPossiblityEnum — Posibilidad de pagos en cuotas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `InstallmentPaymentsPossiblityEnum`
- **Descripción (ES):** Posibilidad de pagos en cuotas
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `ippCr` | 0 | Cr | Crédito |
| `ippNo` | 1 | Number | No |
| `ippRd` | 2 | Rd | Redondeo |
| `ippYes` | 3 | Yes | Sí |

## Used by (1 properties)

- [CreditPaymentMethod](../Entidades/CreditPaymentMethods.md).`InstallmentPaymentsPossible`
