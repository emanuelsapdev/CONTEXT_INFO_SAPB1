# WithholdingTaxLine — Líneas de retenciones

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `WithholdingTaxLine`
- **Descripción (ES):** Líneas de retenciones
- **Description (EN):** Withholding Tax Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 28

## Properties (28)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `WTCode` | Edm.String | Yes | Withholding Tax Code | Código de retención |
| 2 | `WTAmountSys` | Edm.Double | Yes | Withholding Tax Amount (system currency) | Importe de retención (moneda del sistema) |
| 3 | `WTAmountFC` | Edm.Double | Yes | Withholding Tax Amount FC (foreign currency) | Importe de retención (ME) |
| 4 | `WTAmount` | Edm.Double | Yes | Withholding Tax Amount | Importe de retención |
| 5 | `WithholdingType` | Edm.String | Yes | Withholding Type | Tipo de retención |
| 6 | `TaxableAmountinSys` | Edm.Double | Yes | Taxable Amountin (system currency) | Importe imponible (moneda del sistema) |
| 7 | `TaxableAmountFC` | Edm.Double | Yes | Taxable Amount FC (foreign currency) | Importe imponible (ME) |
| 8 | `TaxableAmount` | Edm.Double | Yes | Taxable Amount | Importe imponible |
| 9 | `RoundingType` | Edm.String | Yes | Rounding Type | Tipo de redondeo |
| 10 | `Rate` | Edm.Double | Yes | Rate | Tasa / tipo de cambio |
| 11 | `Criteria` | Edm.String | Yes | Criteria | Criterios |
| 12 | `Category` | Edm.String | Yes | Category | Categoría |
| 13 | `BaseType` | Edm.String | Yes | Base Type | Tipo base (tipo de objeto del documento base) |
| 14 | `AppliedWTAmountSys` | Edm.Double | Yes | Applied Withholding Tax Amount (system currency) | Importe de retención aplicado (moneda del sistema) |
| 15 | `AppliedWTAmountFC` | Edm.Double | Yes | Applied Withholding Tax Amount FC (foreign currency) | Importe de retención aplicado (ME) |
| 16 | `AppliedWTAmount` | Edm.Double | Yes | Applied Withholding Tax Amount | Importe de retención aplicado |
| 17 | `GLAccount` | Edm.String | Yes | G/L Account | Cuenta de mayor |
| 18 | `LineNum` | Edm.Int32 | Yes | Line Number | Número de línea |
| 19 | `BaseDocEntry` | Edm.Int32 | Yes | Base Document Entry | DocEntry del documento base |
| 20 | `BaseDocLine` | Edm.Int32 | Yes | Base Document Line | Línea del documento base |
| 21 | `BaseDocType` | Edm.Int32 | Yes | Base Document Type | Tipo de documento base |
| 22 | `BaseDocumentReference` | Edm.Int32 | Yes | Base Document Reference | Referencia del documento base |
| 23 | `Status` | [BoStatus](../Enums/BoStatus.md) | Yes | Status | Estado |
| 24 | `TargetAbsEntry` | Edm.Int32 | Yes | Target Abs Entry | Entrada absoluta de destino |
| 25 | `TargetDocumentType` | Edm.Int32 | Yes | Target Document Type | Tipo de documento destino |
| 26 | `CSTCodeIncoming` | Edm.String | Yes | CST Code Incoming | Código CST de entrada |
| 27 | `CSTCodeOutgoing` | Edm.String | Yes | CST Code Outgoing | Código CST de salida |
| 28 | `Doc1LineNum` | Edm.Int32 | Yes | Document 1 Line Number | Número de línea del documento 1 |

## Used by (properties)

- [DocumentLine](DocumentLine.md).`WithholdingTaxLines`
