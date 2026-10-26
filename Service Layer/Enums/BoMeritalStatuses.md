# BoMeritalStatuses — Estado civil

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoMeritalStatuses`
- **Descripción (ES):** Estado civil
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `mts_Single` | 0 | Single | Soltero/a |
| `mts_Married` | 1 | Married | Casado/a |
| `mts_Divorced` | 2 | Divorced | Divorciado/a |
| `mts_Widowed` | 3 | Widowed | Viudo/a |
| `mts_NotSpecified` | 4 | Not Specified | No especificado |

## Used by (1 properties)

- [EmployeeInfo](../Entidades/EmployeesInfo.md).`MartialStatus`
