# BoTaxTypes — Tipo de impuesto de la línea

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoTaxTypes`
- **Descripción (ES):** Tipo de impuesto de la línea
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `tt_Yes` | 0 | Yes | Sí (sujeto) |
| `tt_No` | 1 | Number | No (exento) |
| `tt_UseTax` | 2 | Use Tax | Impuesto de uso |
| `tt_OffsetTax` | 3 | Offset Tax | Impuesto de compensación |

## Used by (2 properties)

- [DocumentLine](../Tipos-Complejos/DocumentLine.md).`TaxType`
- [Item](../Entidades/Items.md).`TaxType`
