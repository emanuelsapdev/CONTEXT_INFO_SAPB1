# ExternalCallsService — Servicio de llamadas externas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `ExternalCallsService`
- **Descripción (ES):** Servicio de llamadas externas
- **Operations:** 3

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`ExternalCallsService_GetCall`](#externalcallsservice_getcall) | action | [ExternalCall](../Tipos-Complejos/ExternalCall.md) | Get Call | Obtener llamada |
| [`ExternalCallsService_SendCall`](#externalcallsservice_sendcall) | action | [ExternalCallParams](../Tipos-Complejos/ExternalCallParams.md) | Send Call | Enviar llamada |
| [`ExternalCallsService_UpdateCall`](#externalcallsservice_updatecall) | action | — | Update Call | Actualizar llamada |

## ExternalCallsService_GetCall

- **Descripción (ES):** Obtener llamada
- **Request:** `POST /b1s/v2/ExternalCallsService_GetCall`
- **Parameters:** `ExternalCallParams` ([ExternalCallParams](../Tipos-Complejos/ExternalCallParams.md))
- **Returns:** [ExternalCall](../Tipos-Complejos/ExternalCall.md)

```json
{
  "ExternalCallParams": {
    "ID": 0
  }
}
```

## ExternalCallsService_SendCall

- **Descripción (ES):** Enviar llamada
- **Request:** `POST /b1s/v2/ExternalCallsService_SendCall`
- **Parameters:** `ExternalCall` ([ExternalCall](../Tipos-Complejos/ExternalCall.md))
- **Returns:** [ExternalCallParams](../Tipos-Complejos/ExternalCallParams.md)

```json
{
  "ExternalCall": {
    "ID": 0,
    "Category": 0,
    "CreationDate": "2026-01-31",
    "CreationTime": 0,
    ...
  }
}
```

## ExternalCallsService_UpdateCall

- **Descripción (ES):** Actualizar llamada
- **Request:** `POST /b1s/v2/ExternalCallsService_UpdateCall`
- **Parameters:** `ExternalCall` ([ExternalCall](../Tipos-Complejos/ExternalCall.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "ExternalCall": {
    "ID": 0,
    "Category": 0,
    "CreationDate": "2026-01-31",
    "CreationTime": 0,
    ...
  }
}
```

