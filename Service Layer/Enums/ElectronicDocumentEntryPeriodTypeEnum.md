# ElectronicDocumentEntryPeriodTypeEnum — Tipo de período del documento electrónico

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ElectronicDocumentEntryPeriodTypeEnum`
- **Descripción (ES):** Tipo de período del documento electrónico
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `edeptIgnore` | 0 | Ignore | Ignorar |
| `edeptYear` | 1 | Year | Año |
| `edeptQuarter` | 2 | Quarter | Trimestre |
| `edeptMonth` | 3 | Month | Mes |
| `edeptDateRange` | 4 | Date Range | Rango de fechas |

## Used by (1 properties)

- [EDFEntry](../Tipos-Complejos/EDFEntry.md).`PeriodType`
