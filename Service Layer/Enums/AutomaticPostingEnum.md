# AutomaticPostingEnum — Contabilización automática (reclamaciones)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `AutomaticPostingEnum`
- **Descripción (ES):** Contabilización automática (reclamaciones)
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `apNo` | 0 | Number | No |
| `apInterestAndFee` | 1 | Interest And Fee | Intereses y cargos |
| `apInterestOnly` | 2 | Interest Only | Solo intereses |
| `apFeeOnly` | 3 | Fee Only | Solo cargos |

## Used by (2 properties)

- [BusinessPartner](../Entidades/BusinessPartners.md).`AutomaticPosting`
- [DunningTerm](../Entidades/DunningTerms.md).`AutomaticPosting`
