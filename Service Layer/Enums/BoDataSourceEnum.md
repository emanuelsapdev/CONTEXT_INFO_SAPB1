# BoDataSourceEnum — Origen de datos (diseñador de informes)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoDataSourceEnum`
- **Descripción (ES):** Origen de datos (diseñador de informes)
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `rldsFreeText` | 0 | Free Text | Texto libre |
| `rldsSystemVariable` | 1 | System Variable | Variable del sistema |
| `rldsDatabase` | 2 | Database | Base de datos |
| `rldsFormula` | 3 | Formula | Fórmula |

## Used by (1 properties)

- [ReportLayoutItem](../Tipos-Complejos/ReportLayoutItem.md).`DataSource`
