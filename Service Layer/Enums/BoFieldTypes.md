# BoFieldTypes — Tipo de campo de usuario (UDF)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoFieldTypes`
- **Descripción (ES):** Tipo de campo de usuario (UDF)
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `db_Alpha` | 0 | Alpha | Alfanumérico |
| `db_Memo` | 1 | Memo | Texto (memo) |
| `db_Numeric` | 2 | Numeric | Numérico |
| `db_Date` | 3 | Date | Fecha/hora |
| `db_Float` | 4 | Float | Unidades y totales (decimal) |

## Used by (1 properties)

- [UserFieldMD](../Entidades/UserFieldsMD.md).`Type`
