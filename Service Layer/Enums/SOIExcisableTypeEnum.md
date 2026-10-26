# SOIExcisableTypeEnum — Tipo de impuesto especial SOI

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `SOIExcisableTypeEnum`
- **Descripción (ES):** Tipo de impuesto especial SOI
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `se_Excisable` | 1 | Excisable | Sujeto a impuestos especiales |
| `se_Exemption` | 2 | Exemption | Exención |
| `se_PaidToOther` | 3 | Paid To Other | Pagado a otro |
| `se_NotExcisable` | 4 | Not Excisable | No sujeto |

## Used by (1 properties)

- [Item](../Entidades/Items.md).`SOIExcisable`
