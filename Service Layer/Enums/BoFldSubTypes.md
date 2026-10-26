# BoFldSubTypes — Subtipo de campo de usuario (UDF)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoFldSubTypes`
- **Descripción (ES):** Subtipo de campo de usuario (UDF)
- **Underlying type:** Edm.Int32
- **Members:** 13

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `st_None` | 0 | None | Ninguno |
| `st_Address` | 63 | Address | Dirección |
| `st_Phone` | 35 | Phone | Teléfono |
| `st_Time` | 84 | Time | Hora |
| `st_Rate` | 82 | Rate | Tipo de cambio |
| `st_Sum` | 83 | Sum | Importe |
| `st_Price` | 80 | Price | Precio |
| `st_Quantity` | 81 | Quantity | Cantidad |
| `st_Percentage` | 37 | Percentage | Porcentaje |
| `st_Measurement` | 77 | Measurement | Unidad de medida |
| `st_Link` | 66 | Link | Vínculo |
| `st_Image` | 73 | Image | Imagen |
| `st_Checkbox` | 67 | Checkbox | Casilla de verificación |

## Used by (1 properties)

- [UserFieldMD](../Entidades/UserFieldsMD.md).`SubType`
