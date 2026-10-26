# BoBudgetAlert — Alerta de presupuesto

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoBudgetAlert`
- **Descripción (ES):** Alerta de presupuesto
- **Underlying type:** Edm.Int32
- **Members:** 2

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `ba_AnnualAlert` | 0 | Annual Alert | Alerta anual |
| `ba_MonthlyAlert` | 1 | Monthly Alert | Alerta mensual |

## Used by (1 properties)

- [AdminInfo](../Tipos-Complejos/AdminInfo.md).`BudgetAlert`
