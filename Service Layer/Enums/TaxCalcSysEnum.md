# TaxCalcSysEnum — Sistema de cálculo de impuestos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `TaxCalcSysEnum`
- **Descripción (ES):** Sistema de cálculo de impuestos
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `PreconfiguredFormulaWithJurisdictionSupport` | 0 | Preconfigured Formula With Jurisdiction Support | Fórmula preconfigurada con soporte de jurisdicciones |
| `UserDefinedFormula` | 1 | User Defined Formula | Fórmula definida por el usuario |
| `PreconfiguredFormula` | 2 | Preconfigured Formula | Fórmula preconfigurada |

## Used by (1 properties)

- [CompanyInfo](../Tipos-Complejos/CompanyInfo.md).`TaxCalculationSystem`
