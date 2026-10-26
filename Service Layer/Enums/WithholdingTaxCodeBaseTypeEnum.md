# WithholdingTaxCodeBaseTypeEnum — Tipo de base del código de retención

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `WithholdingTaxCodeBaseTypeEnum`
- **Descripción (ES):** Tipo de base del código de retención
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `wtcbt_Gross` | 0 | Gross | Bruto |
| `wtcbt_Net` | 1 | Net | Neto |
| `wtcbt_VAT` | 2 | VAT | IVA |
| `wtcbt_Gross_VAT` | 3 | Gross VAT | Bruto + IVA |
| `wtcbt_UoM` | 4 | Uo M | Unidad de medida |

## Used by (2 properties)

- [WTDCode](../Entidades/WitholdingTaxDefinition.md).`BaseType`
- [WithholdingTaxCode](../Entidades/WithholdingTaxCodes.md).`BaseType`
