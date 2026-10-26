# TdsTypeEnum — Tipo TDS (India)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `TdsTypeEnum`
- **Descripción (ES):** Tipo TDS (India)
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `wtETds` | 0 | E Tds | e-TDS |
| `wtGstTds` | 1 | Gst Tds | GST TDS |
| `wtGstTcs` | 2 | Gst Tcs | GST TCS |
| `wtTcs` | 3 | Tcs | TCS |

## Used by (1 properties)

- [WithholdingTaxCode](../Entidades/WithholdingTaxCodes.md).`TdsType`
