# EBooksLine — Líneas de libros electrónicos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EBooksLine`
- **Descripción (ES):** Líneas de libros electrónicos
- **Description (EN):** E Books Line

- **Properties:** 15

## Properties (15)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 2 | `NetValue` | Edm.Double | Yes | Net Value | Valor neto |
| 3 | `VatCategory` | Edm.Int32 | Yes | Vat Category | Categoría de IVA |
| 4 | `VatAmount` | Edm.Double | Yes | Vat Amount | Importe de IVA |
| 5 | `WithheldAmount` | Edm.Double | Yes | Withheld Amount | Importe retenido |
| 6 | `WithheldPercentCategory` | Edm.Int32 | Yes | Withheld Percent Category | Categoría de porcentaje retenido |
| 7 | `ExpenseClassificationType` | Edm.Int32 | Yes | Expense Classification Type | Tipo de clasificación de gastos |
| 8 | `ExpenseClassificationCategory` | Edm.Int32 | Yes | Expense Classification Category | Categoría de clasificación de gastos |
| 9 | `VATClassificationType` | Edm.Int32 | Yes | VAT Classification Type | Tipo de clasificación de IVA |
| 10 | `VATClassificationCategory` | Edm.Int32 | Yes | VAT Classification Category | Categoría de clasificación de IVA |
| 11 | `VATExemptionCause` | Edm.Int32 | Yes | VAT Exemption Cause | Causa de exención de IVA |
| 12 | `RecordType` | Edm.Int32 | Yes | Record Type | Tipo de registro |
| 13 | `StampDutyCategory` | Edm.Int32 | Yes | Stamp Duty Category | Categoría de impuesto de timbre |
| 14 | `OtherTaxesCategory` | Edm.Int32 | Yes | Other Taxes Category | Categoría de otros impuestos |
| 15 | `FeesCategory` | Edm.Int32 | Yes | Fees Category | Categoría de cargos |

## Used by (properties)

- [EBooks](../Entidades/EBooks.md).`EBooksLines`
