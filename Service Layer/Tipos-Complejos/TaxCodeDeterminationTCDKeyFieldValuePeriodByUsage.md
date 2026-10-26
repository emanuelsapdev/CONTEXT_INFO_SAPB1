# TaxCodeDeterminationTCDKeyFieldValuePeriodByUsage — Períodos por uso del valor de campo clave TCD

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `TaxCodeDeterminationTCDKeyFieldValuePeriodByUsage`
- **Descripción (ES):** Períodos por uso del valor de campo clave TCD
- **Description (EN):** Tax Code Determination TCD Key Field Value Period By Usage

- **Properties:** 5

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsId` | Edm.Int32 | Yes | Abs ID | ID absoluto |
| 2 | `UsageCode` | Edm.Int32 | Yes | Usage Code | Código de uso |
| 3 | `TaxCode` | Edm.String | Yes | Tax Code | Indicador de impuesto |
| 4 | `ExpTaxCode` | Edm.String | Yes | Exp Tax Code | Indicador de impuesto de gastos |
| 5 | `PurTaxCode` | Edm.String | Yes | Pur Tax Code | Indicador de impuesto de compras |

## Used by (properties)

- [TaxCodeDeterminationTCDKeyFieldValuePeriod](TaxCodeDeterminationTCDKeyFieldValuePeriod.md).`TaxCodeDeterminationTCDKeyFieldValuePeriodByUsages`
