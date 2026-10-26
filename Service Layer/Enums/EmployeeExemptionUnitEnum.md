# EmployeeExemptionUnitEnum — Unidad de exención del empleado

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `EmployeeExemptionUnitEnum`
- **Descripción (ES):** Unidad de exención del empleado
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `eeu_None` | 0 | None | Ninguna |
| `eeu_Yearly` | 1 | Yearly | Anual |
| `eeu_Monthly` | 2 | Monthly | Mensual |
| `eeu_Weekly` | 3 | Weekly | Semanal |
| `eeu_Daily` | 4 | Daily | Diaria |

## Used by (2 properties)

- [EmployeeInfo](../Entidades/EmployeesInfo.md).`AdditionalUnit`
- [EmployeeInfo](../Entidades/EmployeesInfo.md).`ExemptionUnit`
