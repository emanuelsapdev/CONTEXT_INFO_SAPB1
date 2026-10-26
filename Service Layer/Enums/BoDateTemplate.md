# BoDateTemplate — Formato de fecha

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoDateTemplate`
- **Descripción (ES):** Formato de fecha
- **Underlying type:** Edm.Int32
- **Members:** 7

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `dt_DDMMYY` | 0 | DDMMYY | DD/MM/AA |
| `dt_DDMMCCYY` | 1 | DDMMCCYY | DD/MM/AAAA |
| `dt_MMDDYY` | 2 | MMDDYY | MM/DD/AA |
| `dt_MMDDCCYY` | 3 | MMDDCCYY | MM/DD/AAAA |
| `dt_CCYYMMDD` | 4 | CCYYMMDD | AAAA/MM/DD |
| `dt_DDMonthYYYY` | 5 | DD Month YYYY | DD/Mes/AAAA |
| `dt_YYMMDD` | 6 | YYMMDD | AA/MM/DD |

## Used by (1 properties)

- [AdminInfo](../Tipos-Complejos/AdminInfo.md).`DateTemplate`
