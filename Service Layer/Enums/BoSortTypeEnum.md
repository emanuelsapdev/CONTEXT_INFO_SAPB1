# BoSortTypeEnum — Tipo de ordenamiento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoSortTypeEnum`
- **Descripción (ES):** Tipo de ordenamiento
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `rlstAlpha` | 0 | Alpha | Alfabético |
| `rlstNumeric` | 1 | Numeric | Numérico |
| `rlstMoney` | 2 | Money | Monetario |
| `rlstDate` | 3 | Date | Fecha |

## Used by (1 properties)

- [ReportLayoutItem](../Tipos-Complejos/ReportLayoutItem.md).`SortType`
