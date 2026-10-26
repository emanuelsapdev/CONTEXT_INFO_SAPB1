# BoClosingDateProcedureDueMonthEnum — Mes de vencimiento del procedimiento de fecha de cierre

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoClosingDateProcedureDueMonthEnum`
- **Descripción (ES):** Mes de vencimiento del procedimiento de fecha de cierre
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `bocpddm_HalfMonth` | 0 | Half Month | Mitad de mes |
| `bocpddm_MonthEnd` | 1 | Month End | Fin de mes |
| `bocpddm_MonthStart` | 2 | Month Start | Inicio de mes |
| `bocpddm_None` | 3 | None | Ninguno |

## Used by (1 properties)

- [ClosingDateProcedure](../Entidades/ClosingDateProcedure.md).`DueMonth`
