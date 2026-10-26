# PaymentCalculationService — Servicio de cálculo de pagos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `PaymentCalculationService`
- **Descripción (ES):** Servicio de cálculo de pagos
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`PaymentCalculationService_GetPaymentAmount`](#paymentcalculationservice_getpaymentamount) | action | Collection([PaymentAmountParams](../Tipos-Complejos/PaymentAmountParams.md)) | Get Payment Amount | Obtener importe de pago |

## PaymentCalculationService_GetPaymentAmount

- **Descripción (ES):** Obtener importe de pago
- **Request:** `POST /b1s/v2/PaymentCalculationService_GetPaymentAmount`
- **Parameters:** `PaymentBPCode` ([PaymentBPCode](../Tipos-Complejos/PaymentBPCode.md)), `PaymentInvoiceEntries` (Collection([PaymentInvoiceEntry](../Tipos-Complejos/PaymentInvoiceEntry.md)))
- **Returns:** Collection([PaymentAmountParams](../Tipos-Complejos/PaymentAmountParams.md))

```json
{
  "PaymentBPCode": {
    "BPCode": "string",
    "Date": "2026-01-31"
  },
  "PaymentInvoiceEntries": [ {
    "DocEntry": 0,
    "InstallmentId": 0,
    ...
  } ]
}
```

