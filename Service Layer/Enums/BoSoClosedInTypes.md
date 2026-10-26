# BoSoClosedInTypes — Unidad de cierre de la oportunidad

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoSoClosedInTypes`
- **Descripción (ES):** Unidad de cierre de la oportunidad
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `sos_Months` | 0 | Months | Meses |
| `sos_Weeks` | 1 | Weeks | Semanas |
| `sos_Days` | 2 | Days | Días |

## Used by (1 properties)

- [SalesOpportunities](../Entidades/SalesOpportunities.md).`ClosingType`
