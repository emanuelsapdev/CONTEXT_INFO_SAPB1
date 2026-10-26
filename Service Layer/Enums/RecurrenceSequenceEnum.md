# RecurrenceSequenceEnum — Secuencia de recurrencia

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `RecurrenceSequenceEnum`
- **Descripción (ES):** Secuencia de recurrencia
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `rsFirst` | 0 | First | Primero |
| `rsSecond` | 1 | Second | Segundo |
| `rsThird` | 2 | Third | Tercero |
| `rsFourth` | 3 | Fourth | Cuarto |
| `rsLast` | 4 | Last | Último |

## Used by (2 properties)

- [Activity](../Entidades/Activities.md).`RecurrenceSequenceSpecifier`
- [InventoryCycles](../Entidades/InventoryCycles.md).`RecurrenceSequenceSpecifier`
