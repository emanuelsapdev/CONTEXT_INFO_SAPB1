# PaymentMeansTypeEnum — Tipo de medio de pago

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `PaymentMeansTypeEnum`
- **Descripción (ES):** Tipo de medio de pago
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `pmtNotAssigned` | 0 | Not Assigned | No asignado |
| `pmtChecks` | 1 | Checks | Cheques |
| `pmtBankTransfer` | 2 | Bank Transfer | Transferencia bancaria |
| `pmtCash` | 3 | Cash | Efectivo |
| `pmtCreditCard` | 4 | Credit Card | Tarjeta de crédito |

## Used by (1 properties)

- [CashFlowAssignment](../Tipos-Complejos/CashFlowAssignment.md).`PaymentMeans`
