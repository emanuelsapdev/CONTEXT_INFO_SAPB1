# PaymentRunExport_Line — Líneas de exportación de la ejecución de pagos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `PaymentRunExport_Line`
- **Descripción (ES):** Líneas de exportación de la ejecución de pagos
- **Description (EN):** Payment Run Export Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 31

## Properties (31)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `RowNumber` | Edm.Int32 | Yes | Row Number | Número de línea |
| 2 | `DateOfPaymentRun` | Edm.DateTimeOffset | Yes | Date Of Payment Run | Fecha de ejecución de pagos |
| 3 | `PaymentWizardCode` | Edm.Int32 | Yes | Payment Wizard Code | Código del asistente de pagos |
| 4 | `VendorNumber` | Edm.String | Yes | Vendor Number | Número de proveedor |
| 5 | `CustomerNumber` | Edm.String | Yes | Customer Number | Número de cliente |
| 6 | `PaymentMeans` | Edm.String | Yes | Payment Means | Medio de pago |
| 7 | `PaymentDocNum` | Edm.Int32 | Yes | Payment Document Number | Número de documento de pago |
| 8 | `FiscalYear` | Edm.DateTimeOffset | Yes | Fiscal Year | Ejercicio fiscal |
| 9 | `VendorRefNum` | Edm.String | Yes | Vendor Ref Number | N.º de referencia del proveedor |
| 10 | `DocumentObjectType` | Edm.String | Yes | Document Object Type | Tipo de objeto del documento |
| 11 | `DocumentPostingDate` | Edm.DateTimeOffset | Yes | Document Posting Date | Fecha de contabilización del documento |
| 12 | `DocumentTaxDate` | Edm.DateTimeOffset | Yes | Document Tax Date | Fecha de impuestos del documento |
| 13 | `BPDebitPayableAccount` | Edm.String | Yes | Business Partner Debit Payable Account | Cuenta deudora/acreedora del socio de negocios |
| 14 | `DocumentCurrency` | Edm.String | Yes | Document Currency | Moneda del documento |
| 15 | `DocumentRate` | Edm.Double | Yes | Document Rate | Tipo de cambio del documento |
| 16 | `DocumentTotal` | Edm.Double | Yes | Document Total | Total del documento |
| 17 | `DocumentTotalFC` | Edm.Double | Yes | Document Total FC (foreign currency) | Total del documento (ME) |
| 18 | `DocumentTaxAmount` | Edm.Double | Yes | Document Tax Amount | Importe de impuesto del documento |
| 19 | `DocumentTaxAmountFC` | Edm.Double | Yes | Document Tax Amount FC (foreign currency) | Importe de impuesto del documento (ME) |
| 20 | `DocumentRemarks` | Edm.String | Yes | Document Remarks | Comentarios del documento |
| 21 | `DocumentPaymentTerms` | Edm.Int32 | Yes | Document Payment Terms | Condiciones de pago del documento |
| 22 | `PaymentDocReference` | Edm.String | Yes | Payment Document Reference | Referencia del documento de pago |
| 23 | `DocumentLocalCurrency` | Edm.String | Yes | Document Local Currency | Moneda local del documento |
| 24 | `PaymentTermsPeriod` | Edm.Int32 | Yes | Payment Terms Period | Período de las condiciones de pago |
| 25 | `DocumentObjectTypeEx` | Edm.String | Yes | Document Object Type Ex | Tipo de objeto del documento (ampliado) |
| 26 | `DocumentNumber` | Edm.Int32 | Yes | Document Number | Número de documento |
| 27 | `PaymentNumber` | Edm.Int32 | Yes | Payment Number | Número de pago |
| 28 | `PaymentOrderNum` | Edm.Int32 | Yes | Payment Order Number | Número de orden de pago |
| 29 | `FreeText1` | Edm.String | Yes | Free Text 1 | Texto libre 1 |
| 30 | `FreeText2` | Edm.String | Yes | Free Text 2 | Texto libre 2 |
| 31 | `FreeText3` | Edm.String | Yes | Free Text 3 | Texto libre 3 |

## Used by (properties)

- [PaymentRunExport](../Entidades/PaymentRunExport.md).`PaymentRunExport_Lines`
