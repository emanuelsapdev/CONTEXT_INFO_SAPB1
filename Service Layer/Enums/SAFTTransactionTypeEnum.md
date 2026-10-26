# SAFTTransactionTypeEnum — Tipo de transacción SAF-T

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `SAFTTransactionTypeEnum`
- **Descripción (ES):** Tipo de transacción SAF-T
- **Underlying type:** Edm.Int32
- **Members:** 7

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `safttt_Default` | 0 | Default | Predeterminado |
| `safttt_Normal` | 1 | Normal | Normal |
| `safttt_AdjustmentsofTheTaxPeriod` | 2 | Adjustmentsof The Tax Period | Ajustes del período fiscal |
| `safttt_MeasurementofResults` | 3 | Measurementof Results | Medición de resultados |
| `safttt_Adjustment` | 4 | Adjustment | Ajuste |
| `safttt_DoNotExport` | 5 | Do Not Export | No exportar |
| `safttt_NonSystem` | 6 | Non System | No del sistema |

## Used by (1 properties)

- [JournalEntry](../Entidades/JournalEntries.md).`SAFTTransactionType`
