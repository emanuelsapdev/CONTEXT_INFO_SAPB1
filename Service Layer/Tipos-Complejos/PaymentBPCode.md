# PaymentBPCode — Código de socio de negocios del pago

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `PaymentBPCode`
- **Descripción (ES):** Código de socio de negocios del pago
- **Description (EN):** Payment Business Partner Code

- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `BPCode` | Edm.String | Yes | Business Partner Code | Código del socio de negocios |
| 2 | `Date` | Edm.DateTimeOffset | Yes | Date | Fecha |

## Used by (service operations)

- [`PaymentCalculationService_GetPaymentAmount`](../Servicios/PaymentCalculationService.md#paymentcalculationservice_getpaymentamount)
