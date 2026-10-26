# EmployeePaymentMethodEnum — Método de pago al empleado

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `EmployeePaymentMethodEnum`
- **Descripción (ES):** Método de pago al empleado
- **Underlying type:** Edm.Int32
- **Members:** 2

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `epm_None` | 0 | None | Ninguno |
| `epm_BankTransfer` | 1 | Bank Transfer | Transferencia bancaria |

## Used by (1 properties)

- [EmployeeInfo](../Entidades/EmployeesInfo.md).`PaymentMethod`
