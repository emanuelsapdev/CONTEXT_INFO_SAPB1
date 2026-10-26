# EcmActionPeriodTypeEnum — Tipo de período de acción ECM

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `EcmActionPeriodTypeEnum`
- **Descripción (ES):** Tipo de período de acción ECM
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `aptIgnore` | 0 | Ignore | Ignorar |
| `aptYear` | 1 | Year | Año |
| `aptQuarter` | 2 | Quarter | Trimestre |
| `aptMonth` | 3 | Month | Mes |
| `aptDateRange` | 4 | Date Range | Rango de fechas |

## Used by (1 properties)

- [EcmAction](../Tipos-Complejos/EcmAction.md).`PeriodType`
