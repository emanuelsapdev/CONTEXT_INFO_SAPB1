# BoTaxRoundingRuleTypes — Regla de redondeo de impuestos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoTaxRoundingRuleTypes`
- **Descripción (ES):** Regla de redondeo de impuestos
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `trr_RoundDown` | 0 | Round Down | Redondear hacia abajo |
| `trr_RoundUp` | 1 | Round Up | Redondear hacia arriba |
| `trr_RoundOff` | 2 | Round Off | Redondear al más cercano |
| `trr_CompanyDefault` | 3 | Company Default | Predeterminado de la sociedad |

## Used by (1 properties)

- [BusinessPartner](../Entidades/BusinessPartners.md).`TaxRoundingRule`
