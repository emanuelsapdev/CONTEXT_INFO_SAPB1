# PaymentInvoiceEntry — Entrada de factura del pago

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `PaymentInvoiceEntry`
- **Descripción (ES):** Entrada de factura del pago
- **Description (EN):** Payment Invoice Entry

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocType` | [PaymentInvoiceTypeEnum](../Enums/PaymentInvoiceTypeEnum.md) | Yes | Document Type | Tipo de documento (artículos/servicios) |
| 2 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 3 | `InstallmentId` | Edm.Int32 | Yes | Installment ID | ID de cuota |

## Used by (service operations)

- [`PaymentCalculationService_GetPaymentAmount`](../Servicios/PaymentCalculationService.md#paymentcalculationservice_getpaymentamount)
