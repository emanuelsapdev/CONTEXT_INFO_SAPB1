# EBooksDetail — Detalles de libros electrónicos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EBooksDetail`
- **Descripción (ES):** Detalles de libros electrónicos
- **Description (EN):** E Books Detail
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 19

## Properties (19)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `IncomeClassificationType` | Edm.Int32 | Yes | Income Classification Type | Tipo de clasificación de ingresos |
| 2 | `IncomeClassificationCategory` | Edm.Int32 | Yes | Income Classification Category | Categoría de clasificación de ingresos |
| 3 | `ExpensesClassificationType` | Edm.Int32 | Yes | Expenses Classification Type | Tipo de clasificación de gastos |
| 4 | `ExpensesClassificationCategory` | Edm.Int32 | Yes | Expenses Classification Category | Categoría de clasificación de gastos |
| 5 | `NetValueLC` | Edm.Double | Yes | Net Value LC (local currency) | Valor neto (moneda local) |
| 6 | `NetValueFC` | Edm.Double | Yes | Net Value FC (foreign currency) | Valor neto (ME) |
| 7 | `NetValueSC` | Edm.Double | Yes | Net Value SC (system currency) | Valor neto (moneda del sistema) |
| 8 | `VatCategory` | Edm.Int32 | Yes | Vat Category | Categoría de IVA |
| 9 | `WithheldPercentCategory` | Edm.Int32 | Yes | Withheld Percent Category | Categoría de porcentaje retenido |
| 10 | `WithheldAmountLC` | Edm.Double | Yes | Withheld Amount LC (local currency) | Importe retenido (moneda local) |
| 11 | `WithheldAmountFC` | Edm.Double | Yes | Withheld Amount FC (foreign currency) | Importe retenido (ME) |
| 12 | `WithheldAmountSC` | Edm.Double | Yes | Withheld Amount SC (system currency) | Importe retenido (moneda del sistema) |
| 13 | `VatClassificationType` | Edm.Int32 | Yes | Vat Classification Type | Tipo de clasificación de IVA |
| 14 | `VatClassificationCategory` | Edm.Int32 | Yes | Vat Classification Category | Categoría de clasificación de IVA |
| 15 | `VATExemptionCause` | Edm.Int32 | Yes | VAT Exemption Cause | Causa de exención de IVA |
| 16 | `RecType` | Edm.Int32 | Yes | Rec Type | Tipo de registro |
| 17 | `StampDutyCategory` | Edm.Int32 | Yes | Stamp Duty Category | Categoría de impuesto de timbre |
| 18 | `OtherTaxesCategory` | Edm.Int32 | Yes | Other Taxes Category | Categoría de otros impuestos |
| 19 | `FeesCategory` | Edm.Int32 | Yes | Fees Category | Categoría de cargos |

## Used by (properties)

- [DocumentLine](DocumentLine.md).`EBooksDetails`
