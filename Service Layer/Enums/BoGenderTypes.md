# BoGenderTypes — Sexo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoGenderTypes`
- **Descripción (ES):** Sexo
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `gt_Female` | 0 | Female | Femenino |
| `gt_Male` | 1 | Male | Masculino |
| `gt_Undefined` | 2 | Undefined | No definido |
| `gt_Masked` | 3 | Masked | Enmascarado |
| `gt_Invalid` | 4 | Invalid | Inválido |

## Used by (2 properties)

- [ContactEmployee](../Tipos-Complejos/ContactEmployee.md).`Gender`
- [EmployeeInfo](../Entidades/EmployeesInfo.md).`Gender`
