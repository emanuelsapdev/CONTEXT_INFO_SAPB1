# CreditLine — Líneas de tarjetas de crédito

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `CreditLine`
- **Descripción (ES):** Líneas de tarjetas de crédito
- **Description (EN):** Credit Line

- **Properties:** 12

## Properties (12)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsId` | Edm.Int32 | Yes | Abs ID | ID absoluto |
| 2 | `CreditCard` | Edm.Int32 | Yes | Credit Card | Tarjeta de crédito |
| 3 | `VoucherNumber` | Edm.String | Yes | Voucher Number | Número de vale/cupón |
| 4 | `PaymentMethodCode` | Edm.Int32 | Yes | Payment Method Code | Código de vía de pago |
| 5 | `PayDate` | Edm.DateTimeOffset | Yes | Pay Date | Fecha de pago |
| 6 | `Deposited` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Deposited | Depositado |
| 7 | `NumOfPayments` | Edm.Int32 | Yes | Number Of Payments | Cantidad de pagos |
| 8 | `Customer` | Edm.String | Yes | Customer | Cliente |
| 9 | `Reference` | Edm.String | Yes | Reference | Referencia |
| 10 | `Transferred` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Transferred | Transferido |
| 11 | `Total` | Edm.Double | Yes | Total | Total |
| 12 | `CreditCurrency` | Edm.String | Yes | Credit Currency | Moneda del crédito |

## Used by (properties)

- [Deposit](../Entidades/Deposits.md).`CreditLines`

## Used by (service operations)

- [`CreditLinesService_GetCreditLine`](../Servicios/CreditLinesService.md#creditlinesservice_getcreditline)
