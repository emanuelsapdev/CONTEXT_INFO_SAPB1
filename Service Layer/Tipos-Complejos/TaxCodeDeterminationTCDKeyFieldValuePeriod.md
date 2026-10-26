# TaxCodeDeterminationTCDKeyFieldValuePeriod — Períodos del valor de campo clave TCD

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `TaxCodeDeterminationTCDKeyFieldValuePeriod`
- **Descripción (ES):** Períodos del valor de campo clave TCD
- **Description (EN):** Tax Code Determination TCD Key Field Value Period

- **Properties:** 5

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsId` | Edm.Int32 | Yes | Abs ID | ID absoluto |
| 2 | `EfctFrom` | Edm.DateTimeOffset | Yes | Efct From | Vigente desde |
| 3 | `EfctTo` | Edm.DateTimeOffset | Yes | Efct To | Vigente hasta |
| 4 | `TaxCode` | Edm.String | Yes | Tax Code | Indicador de impuesto |
| 5 | `TaxCodeDeterminationTCDKeyFieldValuePeriodByUsages` | Collection([TaxCodeDeterminationTCDKeyFieldValuePeriodByUsage](../Tipos-Complejos/TaxCodeDeterminationTCDKeyFieldValuePeriodByUsage.md)) | Yes | Tax Code Determination TCD Key Field Value Period By Usages | Períodos por uso del valor de campo clave TCD |

## Used by (properties)

- [TaxCodeDeterminationTCDKeyFieldValue](TaxCodeDeterminationTCDKeyFieldValue.md).`TaxCodeDeterminationTCDKeyFieldValuePeriods`
