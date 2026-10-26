# AccountsService — Servicio de cuentas de mayor

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `AccountsService`
- **Descripción (ES):** Servicio de cuentas de mayor
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`AccountsService_CreateOpenBalance`](#accountsservice_createopenbalance) | action | — | Create Open Balance | Crear saldo inicial |

## AccountsService_CreateOpenBalance

- **Descripción (ES):** Crear saldo inicial
- **Request:** `POST /b1s/v2/AccountsService_CreateOpenBalance`
- **Parameters:** `OpenningBalanceAccount` ([OpenningBalanceAccount](../Tipos-Complejos/OpenningBalanceAccount.md)), `GLAccounts` (Collection([GLAccount](../Tipos-Complejos/GLAccount.md)))
- **Returns:** nothing (`204 No Content`)

```json
{
  "OpenningBalanceAccount": {
    "OpenBalanceAccount": "string",
    "Date": "2026-01-31",
    "Ref1": "string",
    "Ref2": "string",
    ...
  },
  "GLAccounts": [ {
    "Code": "string",
    "DueDate": "2026-01-31",
    "Debit": 0.0,
    "Credit": 0.0,
    ...
  } ]
}
```

