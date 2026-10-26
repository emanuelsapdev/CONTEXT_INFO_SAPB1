# ExternalCallStatusEnum — Estado de la llamada externa

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ExternalCallStatusEnum`
- **Descripción (ES):** Estado de la llamada externa
- **Underlying type:** Edm.Int32
- **Members:** 5

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `ecsNew` | 0 | New | Nueva |
| `ecsInProcess` | 1 | In Process | En proceso |
| `ecsCompleted` | 2 | Completed | Completada |
| `ecsConfirmed` | 3 | Confirmed | Confirmada |
| `ecsFailed` | 4 | Failed | Fallida |

## Used by (1 properties)

- [ExternalCall](../Tipos-Complejos/ExternalCall.md).`Status`
