# BillOfExchange — Letra de cambio

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `BillOfExchange`
- **Descripción (ES):** Letra de cambio
- **Description (EN):** Bill Of Exchange
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 28

## Properties (28)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `BillOfExchangeNo` | Edm.Int32 | Yes | Bill Of Exchange Number | Número de letra de cambio |
| 2 | `BillOfExchangeDueDate` | Edm.DateTimeOffset | Yes | Bill Of Exchange Due Date | Fecha de vencimiento de letra de cambio |
| 3 | `Details` | Edm.String | Yes | Details | Detalles |
| 4 | `ReferenceNo` | Edm.String | Yes | Reference Number | Número de referencia |
| 5 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 6 | `PaymentMethodCode` | Edm.String | Yes | Payment Method Code | Código de vía de pago |
| 7 | `BPBankCode` | Edm.String | Yes | Business Partner Bank Code | Código de banco del socio de negocios |
| 8 | `BPBankAct` | Edm.String | Yes | Business Partner Bank Act | Cuenta bancaria del socio de negocios |
| 9 | `BPBankCountry` | Edm.String | Yes | Business Partner Bank Country | País del banco del socio de negocios |
| 10 | `ControlKey` | Edm.String | Yes | Control Key | Clave de control |
| 11 | `PaymentEngineStatus1` | Edm.String | Yes | Payment Engine Status 1 | Estado del motor de pagos 1 |
| 12 | `PaymentEngineStatus2` | Edm.String | Yes | Payment Engine Status 2 | Estado del motor de pagos 2 |
| 13 | `PaymentEngineStatus3` | Edm.String | Yes | Payment Engine Status 3 | Estado del motor de pagos 3 |
| 14 | `StampTaxCode` | Edm.String | Yes | Stamp Tax Code | Código del impuesto de timbre |
| 15 | `StampTaxAmount` | Edm.Double | Yes | Stamp Tax Amount | Importe del impuesto de timbre |
| 16 | `FolioNumber` | Edm.Int32 | Yes | Folio Number | Número de folio |
| 17 | `FolioPrefixString` | Edm.String | Yes | Folio Prefix String | Prefijo de folio (letra) |
| 18 | `InterestAmount` | Edm.Double | Yes | Interest Amount | Importe de intereses |
| 19 | `DiscountAmount` | Edm.Double | Yes | Discount Amount | Importe de descuento |
| 20 | `FineAmount` | Edm.Double | Yes | Fine Amount | Importe de multa |
| 21 | `InterestDate` | Edm.DateTimeOffset | Yes | Interest Date | Fecha de intereses |
| 22 | `DiscountDate` | Edm.DateTimeOffset | Yes | Discount Date | Fecha de descuento |
| 23 | `FineDate` | Edm.DateTimeOffset | Yes | Fine Date | Fecha de multa |
| 24 | `IOFAmount` | Edm.Double | Yes | IOF Amount | Importe de IOF (Brasil) |
| 25 | `ServiceFeeAmount` | Edm.Double | Yes | Service Fee Amount | Importe de tarifa de servicio |
| 26 | `OtherExpensesAmount` | Edm.Double | Yes | Other Expenses Amount | Importe de otros gastos |
| 27 | `OtherIncomesAmount` | Edm.Double | Yes | Other Incomes Amount | Importe de otros ingresos |
| 28 | `LastPageFolioNumber` | Edm.Int32 | Yes | Last Page Folio Number | Número de folio de la última página |

## Used by (properties)

- [Payment](../Entidades/VendorPayments.md).`BillOfExchange`
