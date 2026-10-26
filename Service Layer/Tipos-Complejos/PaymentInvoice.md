# PaymentInvoice — Facturas del pago

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `PaymentInvoice`
- **Descripción (ES):** Facturas del pago
- **Description (EN):** Payment Invoice
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 24

## Properties (24)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineNum` | Edm.Int32 | Yes | Line Number | Número de línea |
| 2 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 3 | `DocNum` | Edm.Int32 | Yes | Document Number | Número de documento |
| 4 | `SumApplied` | Edm.Double | Yes | Sum Applied | Importe aplicado |
| 5 | `AppliedFC` | Edm.Double | Yes | Applied FC (foreign currency) | Aplicado (ME) |
| 6 | `AppliedSys` | Edm.Double | Yes | Applied (system currency) | Aplicado (moneda del sistema) |
| 7 | `DocRate` | Edm.Double | Yes | Document Rate | Tipo de cambio del documento |
| 8 | `DocLine` | Edm.Int32 | Yes | Document Line | Línea del documento |
| 9 | `InvoiceType` | [BoRcptInvTypes](../Enums/BoRcptInvTypes.md) | Yes | Invoice Type | Tipo de factura |
| 10 | `DiscountPercent` | Edm.Double | Yes | Discount Percent | Porcentaje de descuento |
| 11 | `PaidSum` | Edm.Double | Yes | Paid Sum | Importe pagado |
| 12 | `InstallmentId` | Edm.Int32 | Yes | Installment ID | ID de cuota |
| 13 | `WitholdingTaxApplied` | Edm.Double | Yes | Witholding Tax Applied | Retención aplicada |
| 14 | `WitholdingTaxAppliedFC` | Edm.Double | Yes | Witholding Tax Applied FC (foreign currency) | Retención aplicada (ME) |
| 15 | `WitholdingTaxAppliedSC` | Edm.Double | Yes | Witholding Tax Applied SC (system currency) | Retención aplicada (moneda del sistema) |
| 16 | `LinkDate` | Edm.DateTimeOffset | Yes | Link Date | Fecha de vínculo |
| 17 | `DistributionRule` | Edm.String | Yes | Distribution Rule | Norma de reparto |
| 18 | `DistributionRule2` | Edm.String | Yes | Distribution Rule 2 | Norma de reparto 2 |
| 19 | `DistributionRule3` | Edm.String | Yes | Distribution Rule 3 | Norma de reparto 3 |
| 20 | `DistributionRule4` | Edm.String | Yes | Distribution Rule 4 | Norma de reparto 4 |
| 21 | `DistributionRule5` | Edm.String | Yes | Distribution Rule 5 | Norma de reparto 5 |
| 22 | `TotalDiscount` | Edm.Double | Yes | Total Discount | Descuento total |
| 23 | `TotalDiscountFC` | Edm.Double | Yes | Total Discount FC (foreign currency) | Descuento total (ME) |
| 24 | `TotalDiscountSC` | Edm.Double | Yes | Total Discount SC (system currency) | Descuento total (moneda del sistema) |

## Used by (properties)

- [Payment](../Entidades/VendorPayments.md).`PaymentInvoices`
