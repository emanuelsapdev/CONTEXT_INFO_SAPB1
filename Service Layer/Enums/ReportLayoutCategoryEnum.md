# ReportLayoutCategoryEnum — Categoría del formato de informe

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ReportLayoutCategoryEnum`
- **Descripción (ES):** Categoría del formato de informe
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `rlcPLD` | 0 | PLD | Print Layout Designer |
| `rlcCrystal` | 1 | Crystal | Crystal Reports |
| `rlcLegalList` | 2 | Legal List | Lista legal |
| `rlcUserDefinedType` | 3 | User Defined Type | Tipo definido por el usuario |

## Used by (2 properties)

- [ReportLayout](../Tipos-Complejos/ReportLayout.md).`Category`
- [ReportLayoutParams](../Tipos-Complejos/ReportLayoutParams.md).`Category`
