# DepositsService — Servicio de depósitos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `DepositsService`
- **Descripción (ES):** Servicio de depósitos
- **Operations:** 3

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`DepositsService_CancelCheckRow`](#depositsservice_cancelcheckrow) | action | — | Cancel Check Row | Cancelar línea de cheque |
| [`DepositsService_CancelCheckRowbyCurrentSystemDate`](#depositsservice_cancelcheckrowbycurrentsystemdate) | action | — | Cancel Check Rowby Current System Date | Cancelar línea de cheque con fecha actual del sistema |
| [`DepositsService_GetDepositList`](#depositsservice_getdepositlist) | action | Collection([DepositParams](../Tipos-Complejos/DepositParams.md)) | Get Deposit List | Obtener lista de depósitos |

## DepositsService_CancelCheckRow

- **Descripción (ES):** Cancelar línea de cheque
- **Request:** `POST /b1s/v2/DepositsService_CancelCheckRow`
- **Parameters:** `CancelCheckRowParams` ([CancelCheckRowParams](../Tipos-Complejos/CancelCheckRowParams.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "CancelCheckRowParams": {
    "DepositID": 0,
    "CheckID": 0
  }
}
```

## DepositsService_CancelCheckRowbyCurrentSystemDate

- **Descripción (ES):** Cancelar línea de cheque con fecha actual del sistema
- **Request:** `POST /b1s/v2/DepositsService_CancelCheckRowbyCurrentSystemDate`
- **Parameters:** `CancelCheckRowParams` ([CancelCheckRowParams](../Tipos-Complejos/CancelCheckRowParams.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "CancelCheckRowParams": {
    "DepositID": 0,
    "CheckID": 0
  }
}
```

## DepositsService_GetDepositList

- **Descripción (ES):** Obtener lista de depósitos
- **Request:** `POST /b1s/v2/DepositsService_GetDepositList`
- **Parameters:** none
- **Returns:** Collection([DepositParams](../Tipos-Complejos/DepositParams.md))

