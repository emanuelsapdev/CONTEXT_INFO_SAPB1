# BoPictureSizeEnum — Tamaño de imagen

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoPictureSizeEnum`
- **Descripción (ES):** Tamaño de imagen
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `rlpsOriginalSize` | 0 | Original Size | Tamaño original |
| `rlpsFitFieldSizeNonProportionally` | 1 | Fit Field Size Non Proportionally | Ajustar al campo (no proporcional) |
| `rlpsFitFieldSizeProportionally` | 2 | Fit Field Size Proportionally | Ajustar al campo (proporcional) |
| `rlpsFitFieldHeight` | 3 | Fit Field Height | Ajustar a la altura del campo |
| `rlpsFitFieldWidth` | 4 | Fit Field Width | Ajustar al ancho del campo |

## Used by (1 properties)

- [ReportLayoutItem](../Tipos-Complejos/ReportLayoutItem.md).`PictureSize`
