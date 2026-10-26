# JournalVouchersService — Servicio de comprobantes de asiento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `JournalVouchersService`
- **Descripción (ES):** Servicio de comprobantes de asiento
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`JournalVouchersService_Add`](#journalvouchersservice_add) | action | — | Add | Agregar |

## JournalVouchersService_Add

- **Descripción (ES):** Agregar
- **Request:** `POST /b1s/v2/JournalVouchersService_Add`
- **Parameters:** `JournalVoucher` (Collection([JournalEntry](../Entidades/JournalEntries.md)))
- **Returns:** nothing (`204 No Content`)

```json
{
  "JournalVoucher": [ {
    "ReferenceDate": "2026-01-31",
    "Memo": "string",
    "Reference": "string",
    "Reference2": "string",
    ...
  } ]
}
```

