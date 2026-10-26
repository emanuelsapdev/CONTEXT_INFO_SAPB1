# TaxTypeBlackListEnum — Lista negra de tipos de impuesto

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `TaxTypeBlackListEnum`
- **Descripción (ES):** Lista negra de tipos de impuesto
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `ttblExcluded` | 0 | Excluded | Excluido |
| `ttblExempt` | 1 | Exempt | Exento |
| `ttblNonSubject` | 2 | Non Subject | No sujeto |
| `ttblNotTaxable` | 3 | Not Taxable | No imponible |
| `ttblTaxable` | 4 | Taxable | Imponible |

## Used by (1 properties)

- [VatGroup](../Entidades/VatGroups.md).`TaxTypeBlackList`
