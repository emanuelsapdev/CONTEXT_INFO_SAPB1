# PaymentBlockParams — Parámetros de bloqueos de pago

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `PaymentBlockParams`
- **Descripción (ES):** Parámetros de bloqueos de pago
- **Description (EN):** Payment Block Parameters

- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` | Edm.Int32 | Yes | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `PaymentBlockCode` | Edm.String | Yes | Payment Block Code | Código de bloqueo de pago |

## Used by (service operations)

- [`PaymentBlocksService_GetPaymentBlockList`](../Servicios/PaymentBlocksService.md#paymentblocksservice_getpaymentblocklist)
