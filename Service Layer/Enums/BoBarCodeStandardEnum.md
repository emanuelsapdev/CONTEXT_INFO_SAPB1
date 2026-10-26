# BoBarCodeStandardEnum — Estándar de código de barras

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoBarCodeStandardEnum`
- **Descripción (ES):** Estándar de código de barras
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `rlbsan13` | 0 | Rlbsan 13 | EAN-13 |
| `rlbsCode39` | 1 | Code 39 | Code 39 |
| `rlbsCode128` | 2 | Code 128 | Code 128 |

## Used by (1 properties)

- [ReportLayoutItem](../Tipos-Complejos/ReportLayoutItem.md).`BarCodeStandard`
