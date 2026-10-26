# PaymentAmountParams — Parámetros de importe de pago

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `PaymentAmountParams`
- **Descripción (ES):** Parámetros de importe de pago
- **Description (EN):** Payment Amount Parameters

- **Properties:** 10

## Properties (10)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocType` | [PaymentInvoiceTypeEnum](../Enums/PaymentInvoiceTypeEnum.md) | Yes | Document Type | Tipo de documento (artículos/servicios) |
| 2 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 3 | `InstallmentId` | Edm.Int32 | Yes | Installment ID | ID de cuota |
| 4 | `CashDiscountPercentage` | Edm.Double | Yes | Cash Discount Percentage | Porcentaje de descuento por pronto pago |
| 5 | `CashDiscountAmount` | Edm.Double | Yes | Cash Discount Amount | Importe de descuento por pronto pago |
| 6 | `CashDiscountAmountFC` | Edm.Double | Yes | Cash Discount Amount FC (foreign currency) | Importe de descuento por pronto pago (ME) |
| 7 | `CashDiscountAmountSC` | Edm.Double | Yes | Cash Discount Amount SC (system currency) | Importe de descuento por pronto pago (moneda del sistema) |
| 8 | `TotalPaymentAmount` | Edm.Double | Yes | Total Payment Amount | Importe total del pago |
| 9 | `TotalPaymentAmountFC` | Edm.Double | Yes | Total Payment Amount FC (foreign currency) | Importe total del pago (ME) |
| 10 | `TotalPaymentAmountSC` | Edm.Double | Yes | Total Payment Amount SC (system currency) | Importe total del pago (moneda del sistema) |

## Used by (service operations)

- [`PaymentCalculationService_GetPaymentAmount`](../Servicios/PaymentCalculationService.md#paymentcalculationservice_getpaymentamount)
