# BankStatementsService — Servicio de extractos bancarios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `BankStatementsService`
- **Descripción (ES):** Servicio de extractos bancarios
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`BankStatementsService_GetBankStatementList`](#bankstatementsservice_getbankstatementlist) | action | Collection([BankStatementParams](../Tipos-Complejos/BankStatementParams.md)) | Get Bank Statement List | Obtener lista de extractos bancarios |

## BankStatementsService_GetBankStatementList

- **Descripción (ES):** Obtener lista de extractos bancarios
- **Request:** `POST /b1s/v2/BankStatementsService_GetBankStatementList`
- **Parameters:** `BankStatementsFilter` ([BankStatementsFilter](../Tipos-Complejos/BankStatementsFilter.md))
- **Returns:** Collection([BankStatementParams](../Tipos-Complejos/BankStatementParams.md))

```json
{
  "BankStatementsFilter": {
    "Country": "string",
    "Bank": "string",
    "Account": "string"
  }
}
```

