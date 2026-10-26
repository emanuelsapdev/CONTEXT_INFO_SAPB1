# SAFTTaxCodeEnum — Código de impuesto SAF-T

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `SAFTTaxCodeEnum`
- **Descripción (ES):** Código de impuesto SAF-T
- **Underlying type:** Edm.Int32
- **Members:** 6

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `safttc_ReducedTax` | 0 | Reduced Tax | Tasa reducida |
| `safttc_MiddleTax` | 1 | Middle Tax | Tasa intermedia |
| `safttc_NormalTax` | 2 | Normal Tax | Tasa normal |
| `safttc_Exempt` | 3 | Exempt | Exento |
| `safttt_Others` | 4 | Others | Otros |
| `safttc_NonSystem` | 5 | Non System | No del sistema |

## Used by (1 properties)

- [VatGroup](../Entidades/VatGroups.md).`SAFTTaxCode`
