# BoSubPeriodTypeEnum — Tipo de subperíodo contable

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoSubPeriodTypeEnum`
- **Descripción (ES):** Tipo de subperíodo contable
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `spt_Year` | 0 | Year | Año |
| `spt_Quarters` | 1 | Quarters | Trimestres |
| `spt_Months` | 2 | Months | Meses |
| `spt_Days` | 3 | Days | Días |

## Used by (2 properties)

- [GLAccountAdvancedRule](../Entidades/GLAccountAdvancedRules.md).`SubPeriodType`
- [PeriodCategory](../Tipos-Complejos/PeriodCategory.md).`SubPeriodType`
