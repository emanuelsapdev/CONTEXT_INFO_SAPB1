# BoFrequencyTypeEnum — Tipo de frecuencia

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoFrequencyTypeEnum`
- **Descripción (ES):** Tipo de frecuencia
- **Underlying type:** Edm.Int32
- **Members:** 9

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `ftDaily` | 0 | Daily | Diaria |
| `ftWeekly` | 1 | Weekly | Semanal |
| `ftMonthly` | 2 | Monthly | Mensual |
| `ftQuarterly` | 3 | Quarterly | Trimestral |
| `ftSemiannually` | 4 | Semiannually | Semestral |
| `ftAnnually` | 5 | Annually | Anual |
| `ftOneTime` | 6 | One Time | Una vez |
| `ftTemplate` | 7 | Template | Plantilla |
| `ftNotExecuted` | 8 | Not Executed | No ejecutado |

## Used by (1 properties)

- [RecurringPostings](../Entidades/RecurringPostings.md).`Frequency`
