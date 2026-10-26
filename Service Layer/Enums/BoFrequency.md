# BoFrequency — Frecuencia

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `BoFrequency`
- **Descripción (ES):** Frecuencia
- **Underlying type:** Edm.Int32
- **Members:** 9

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `bof_Daily` | 0 | Daily | Diaria |
| `bof_Weekly` | 1 | Weekly | Semanal |
| `bof_Every4Weeks` | 2 | Every 4 Weeks | Cada 4 semanas |
| `bof_Monthly` | 3 | Monthly | Mensual |
| `bof_Quarterly` | 4 | Quarterly | Trimestral |
| `bof_HalfYearly` | 5 | Half Yearly | Semestral |
| `bof_Annually` | 6 | Annually | Anual |
| `bof_OneTime` | 7 | One Time | Una vez |
| `bof_EveryXDays` | 8 | Every X Days | Cada X días |

## Used by (1 properties)

- [InventoryCycles](../Entidades/InventoryCycles.md).`Frequency`
