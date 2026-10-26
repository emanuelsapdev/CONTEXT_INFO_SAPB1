# BoHorizontalAlignmentEnum — Alineación horizontal

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoHorizontalAlignmentEnum`
- **Descripción (ES):** Alineación horizontal
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `rlhjRight` | 0 | Right | Derecha |
| `rlhjLeft` | 1 | Left | Izquierda |
| `rlhjCentralized` | 2 | Centralized | Centrada |
| `rlhjLanguageDependent` | 3 | Language Dependent | Según el idioma |

## Used by (1 properties)

- [ReportLayoutItem](../Tipos-Complejos/ReportLayoutItem.md).`HorizontalAlignment`
