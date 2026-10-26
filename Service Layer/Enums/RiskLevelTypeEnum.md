# RiskLevelTypeEnum — Nivel de riesgo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `RiskLevelTypeEnum`
- **Descripción (ES):** Nivel de riesgo
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `rlt_Low` | 0 | Low | Bajo |
| `rlt_Medium` | 1 | Medium | Medio |
| `rlt_High` | 2 | High | Alto |

## Used by (1 properties)

- [PM_ProjectDocumentData](../Entidades/ProjectManagements.md).`RiskLevel`
