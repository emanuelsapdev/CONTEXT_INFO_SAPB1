# SEPASequenceTypeEnum — Tipo de secuencia SEPA

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `SEPASequenceTypeEnum`
- **Descripción (ES):** Tipo de secuencia SEPA
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `sstOOFF` | 0 | OOFF | Único (OOFF) |
| `sstFRST` | 1 | FRST | Primero (FRST) |
| `sstRCUR` | 2 | RCUR | Recurrente (RCUR) |
| `sstFNAL` | 3 | FNAL | Final (FNAL) |

## Used by (1 properties)

- [BPBankAccount](../Tipos-Complejos/BPBankAccount.md).`SEPASeqType`
