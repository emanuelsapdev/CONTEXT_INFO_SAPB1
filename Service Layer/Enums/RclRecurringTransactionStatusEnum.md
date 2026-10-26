# RclRecurringTransactionStatusEnum — Estado de la transacción recurrente

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `RclRecurringTransactionStatusEnum`
- **Descripción (ES):** Estado de la transacción recurrente
- **Underlying type:** Edm.Int32
- **Members:** 3

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `rtsNotExecuted` | 1 | Not Executed | No ejecutada |
| `rtsExecuted` | 2 | Executed | Ejecutada |
| `rtsRemoved` | 3 | Removed | Eliminada |

## Used by (1 properties)

- [RclRecurringTransaction](../Tipos-Complejos/RclRecurringTransaction.md).`Status`
