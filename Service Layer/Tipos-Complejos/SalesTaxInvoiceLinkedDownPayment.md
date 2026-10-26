# SalesTaxInvoiceLinkedDownPayment — Anticipos vinculados de la factura de impuestos de venta

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `SalesTaxInvoiceLinkedDownPayment`
- **Descripción (ES):** Anticipos vinculados de la factura de impuestos de venta
- **Description (EN):** Sales Tax Invoice Linked Down Payment
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 21

## Properties (21)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 2 | `LineNum` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `DownPaymentType` | Edm.Int32 | Yes | Down Payment Type | Tipo de anticipo |
| 4 | `DownPaymentEntry` | Edm.Int32 | Yes | Down Payment Entry | Entrada del anticipo |
| 5 | `DownPaymentNum` | Edm.Int32 | Yes | Down Payment Number | Número de anticipo |
| 6 | `PaymentType` | Edm.Int32 | Yes | Payment Type | Tipo de pago |
| 7 | `PaymentEntry` | Edm.Int32 | Yes | Payment Entry | Entrada del pago |
| 8 | `PaymentNum` | Edm.Int32 | Yes | Payment Number | Número de pago |
| 9 | `PaymentTaxDate` | Edm.DateTimeOffset | Yes | Payment Tax Date | Fecha de impuestos del pago |
| 10 | `TransferDate` | Edm.DateTimeOffset | Yes | Transfer Date | Fecha de transferencia |
| 11 | `TransferReference` | Edm.String | Yes | Transfer Reference | Referencia de la transferencia |
| 12 | `AmountToDraw` | Edm.Double | Yes | Amount To Draw | Importe a utilizar |
| 13 | `AmountToDrawFC` | Edm.Double | Yes | Amount To Draw FC (foreign currency) | Importe a utilizar (ME) |
| 14 | `AmountToDrawSC` | Edm.Double | Yes | Amount To Draw SC (system currency) | Importe a utilizar (moneda del sistema) |
| 15 | `Tax` | Edm.Double | Yes | Tax | Impuesto |
| 16 | `TaxFC` | Edm.Double | Yes | Tax FC (foreign currency) | Impuestos (ME) |
| 17 | `TaxSC` | Edm.Double | Yes | Tax SC (system currency) | Impuestos (moneda del sistema) |
| 18 | `GrossAmountToDraw` | Edm.Double | Yes | Gross Amount To Draw | Importe bruto a utilizar |
| 19 | `GrossAmountToDrawFC` | Edm.Double | Yes | Gross Amount To Draw FC (foreign currency) | Importe bruto a utilizar (ME) |
| 20 | `GrossAmountToDrawSC` | Edm.Double | Yes | Gross Amount To Draw SC (system currency) | Importe bruto a utilizar (moneda del sistema) |
| 21 | `DocCurrency` | Edm.String | Yes | Document Currency | Moneda del documento |

## Used by (properties)

- [SalesTaxInvoice](../Entidades/SalesTaxInvoices.md).`SalesTaxInvoiceLinkedDownPayments`
