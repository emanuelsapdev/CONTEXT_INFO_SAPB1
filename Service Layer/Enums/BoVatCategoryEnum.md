# BoVatCategoryEnum — Categoría de IVA

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoVatCategoryEnum`
- **Descripción (ES):** Categoría de IVA
- **Underlying type:** Edm.Int32
- **Members:** 2

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `bovcInputTax` | 0 | Input Tax | IVA soportado (compras) |
| `bovcOutputTax` | 1 | Output Tax | IVA repercutido (ventas) |

## Used by (2 properties)

- [DeductibleTax](../Entidades/DeductibleTaxes.md).`Category`
- [VatGroup](../Entidades/VatGroups.md).`Category`
