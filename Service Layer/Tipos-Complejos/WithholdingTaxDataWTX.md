# WithholdingTaxDataWTX — Datos de retención WTX

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `WithholdingTaxDataWTX`
- **Descripción (ES):** Datos de retención WTX
- **Description (EN):** Withholding Tax Data WTX
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 32

## Properties (32)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `WTAmountSys` | Edm.Double | Yes | Withholding Tax Amount (system currency) | Importe de retención (moneda del sistema) |
| 2 | `WTAmountFC` | Edm.Double | Yes | Withholding Tax Amount FC (foreign currency) | Importe de retención (ME) |
| 3 | `WTAmount` | Edm.Double | Yes | Withholding Tax Amount | Importe de retención |
| 4 | `WithholdingType` | Edm.String | Yes | Withholding Type | Tipo de retención |
| 5 | `TaxableAmountinSys` | Edm.Double | Yes | Taxable Amountin (system currency) | Importe imponible (moneda del sistema) |
| 6 | `TaxableAmountFC` | Edm.Double | Yes | Taxable Amount FC (foreign currency) | Importe imponible (ME) |
| 7 | `TaxableAmount` | Edm.Double | Yes | Taxable Amount | Importe imponible |
| 8 | `Rate` | Edm.Double | Yes | Rate | Tasa / tipo de cambio |
| 9 | `Category` | Edm.String | Yes | Category | Categoría |
| 10 | `BaseType` | Edm.String | Yes | Base Type | Tipo base (tipo de objeto del documento base) |
| 11 | `AppliedWTAmountSys` | Edm.Double | Yes | Applied Withholding Tax Amount (system currency) | Importe de retención aplicado (moneda del sistema) |
| 12 | `AppliedWTAmountFC` | Edm.Double | Yes | Applied Withholding Tax Amount FC (foreign currency) | Importe de retención aplicado (ME) |
| 13 | `AppliedWTAmount` | Edm.Double | Yes | Applied Withholding Tax Amount | Importe de retención aplicado |
| 14 | `GLAccount` | Edm.String | Yes | G/L Account | Cuenta de mayor |
| 15 | `LineNum` | Edm.Int32 | Yes | Line Number | Número de línea |
| 16 | `BaseDocEntry` | Edm.Int32 | Yes | Base Document Entry | DocEntry del documento base |
| 17 | `BaseDocLine` | Edm.Int32 | Yes | Base Document Line | Línea del documento base |
| 18 | `BaseDocType` | Edm.String | Yes | Base Document Type | Tipo de documento base |
| 19 | `WTAbsId` | Edm.String | Yes | Withholding Tax Abs ID | ID absoluto de retención |
| 20 | `ExemptRate` | Edm.Double | Yes | Exempt Rate | Tasa exenta |
| 21 | `BaseNetAmountSys` | Edm.Double | Yes | Base Net Amount (system currency) | Importe neto base (moneda del sistema) |
| 22 | `BaseNetAmountFC` | Edm.Double | Yes | Base Net Amount FC (foreign currency) | Importe neto base (ME) |
| 23 | `BaseNetAmount` | Edm.Double | Yes | Base Net Amount | Importe neto base |
| 24 | `BaseVatmountSys` | Edm.Double | Yes | Base Vatmount (system currency) | Importe base de IVA (moneda del sistema) |
| 25 | `BaseVatmountFC` | Edm.Double | Yes | Base Vatmount FC (foreign currency) | Importe base de IVA (ME) |
| 26 | `BaseVatmount` | Edm.Double | Yes | Base Vatmount | Importe base de IVA |
| 27 | `AccumBaseAmountSys` | Edm.Double | Yes | Accum Base Amount (system currency) | Importe base acumulado (moneda del sistema) |
| 28 | `AccumBaseAmountFC` | Edm.Double | Yes | Accum Base Amount FC (foreign currency) | Importe base acumulado (ME) |
| 29 | `AccumBaseAmount` | Edm.Double | Yes | Accum Base Amount | Importe base acumulado |
| 30 | `AccumWTaxAmountSys` | Edm.Double | Yes | Accum W Tax Amount (system currency) | Importe de retención acumulado (moneda del sistema) |
| 31 | `AccumWTaxAmountFC` | Edm.Double | Yes | Accum W Tax Amount FC (foreign currency) | Importe de retención acumulado (ME) |
| 32 | `AccumWTaxAmount` | Edm.Double | Yes | Accum W Tax Amount | Importe de retención acumulado |

## Used by (properties)

- [Document](../Entidades/PurchaseQuotations.md).`WithholdingTaxDataWTXCollection`
- [Payment](../Entidades/VendorPayments.md).`WithholdingTaxDataWTXCollection`
