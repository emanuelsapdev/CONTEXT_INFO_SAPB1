# RecurringTransactionTemplateFrequencyEnum — Frecuencia de la plantilla de transacción recurrente

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `RecurringTransactionTemplateFrequencyEnum`
- **Descripción (ES):** Frecuencia de la plantilla de transacción recurrente
- **Underlying type:** Edm.Int32
- **Members:** 9

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `rttf_Daily` | 0 | Daily | Diaria |
| `rttf_Weekly` | 1 | Weekly | Semanal |
| `rttf_Every2Weeks` | 2 | Every 2 Weeks | Cada 2 semanas |
| `rttf_Monthly` | 3 | Monthly | Mensual |
| `rttf_Every2Months` | 4 | Every 2 Months | Cada 2 meses |
| `rttf_Quarterly` | 5 | Quarterly | Trimestral |
| `rttf_Semiannually` | 6 | Semiannually | Semestral |
| `rttf_Annually` | 7 | Annually | Anual |
| `rttf_OneTime` | 8 | One Time | Una vez |

## Used by (1 properties)

- [RecurringTransactionTemplate](../Entidades/RecurringTransactionTemplates.md).`Frequency`
