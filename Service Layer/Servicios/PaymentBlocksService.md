# PaymentBlocksService — Servicio de bloqueos de pago

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `PaymentBlocksService`
- **Descripción (ES):** Servicio de bloqueos de pago
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`PaymentBlocksService_GetPaymentBlockList`](#paymentblocksservice_getpaymentblocklist) | action | Collection([PaymentBlockParams](../Tipos-Complejos/PaymentBlockParams.md)) | Get Payment Block List | Obtener lista de bloqueos de pago |

## PaymentBlocksService_GetPaymentBlockList

- **Descripción (ES):** Obtener lista de bloqueos de pago
- **Request:** `POST /b1s/v2/PaymentBlocksService_GetPaymentBlockList`
- **Parameters:** none
- **Returns:** Collection([PaymentBlockParams](../Tipos-Complejos/PaymentBlockParams.md))

