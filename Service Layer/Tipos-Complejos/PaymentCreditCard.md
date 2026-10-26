# PaymentCreditCard — Tarjetas de crédito del pago

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `PaymentCreditCard`
- **Descripción (ES):** Tarjetas de crédito del pago
- **Description (EN):** Payment Credit Card
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 20

## Properties (20)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineNum` | Edm.Int32 | Yes | Line Number | Número de línea |
| 2 | `CreditCard` | Edm.Int32 | Yes | Credit Card | Tarjeta de crédito |
| 3 | `CreditAcct` | Edm.String | Yes | Credit Account | Cuenta de haber |
| 4 | `CreditCardNumber` | Edm.String | Yes | Credit Card Number | Número de tarjeta de crédito |
| 5 | `CardValidUntil` | Edm.DateTimeOffset | Yes | Card Valid Until | Tarjeta válida hasta |
| 6 | `VoucherNum` | Edm.String | Yes | Voucher Number | Número de vale/cupón |
| 7 | `OwnerIdNum` | Edm.String | Yes | Owner ID Number | N.º de identificación del titular |
| 8 | `OwnerPhone` | Edm.String | Yes | Owner Phone | Teléfono del titular |
| 9 | `PaymentMethodCode` | Edm.Int32 | Yes | Payment Method Code | Código de vía de pago |
| 10 | `NumOfPayments` | Edm.Int32 | Yes | Number Of Payments | Cantidad de pagos |
| 11 | `FirstPaymentDue` | Edm.DateTimeOffset | Yes | First Payment Due | Vencimiento del primer pago |
| 12 | `FirstPaymentSum` | Edm.Double | Yes | First Payment Sum | Importe del primer pago |
| 13 | `AdditionalPaymentSum` | Edm.Double | Yes | Additional Payment Sum | Importe de pago adicional |
| 14 | `CreditSum` | Edm.Double | Yes | Credit Sum | Importe de tarjeta de crédito |
| 15 | `CreditCur` | Edm.String | Yes | Credit Currency | Moneda del crédito |
| 16 | `CreditRate` | Edm.Double | Yes | Credit Rate | Tasa de crédito |
| 17 | `ConfirmationNum` | Edm.String | Yes | Confirmation Number | Número de confirmación |
| 18 | `NumOfCreditPayments` | Edm.Int32 | Yes | Number Of Credit Payments | Cantidad de pagos con tarjeta |
| 19 | `CreditType` | [BoRcptCredTypes](../Enums/BoRcptCredTypes.md) | Yes | Credit Type | Tipo de crédito |
| 20 | `SplitPayments` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Split Payments | Pagos divididos |

## Used by (properties)

- [Payment](../Entidades/VendorPayments.md).`PaymentCreditCards`
