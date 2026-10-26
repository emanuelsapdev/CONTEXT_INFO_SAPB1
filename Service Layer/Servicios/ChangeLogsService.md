# ChangeLogsService — Servicio de registro de modificaciones

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `ChangeLogsService`
- **Descripción (ES):** Servicio de registro de modificaciones
- **Operations:** 2

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`ChangeLogsService_GetChangeLog`](#changelogsservice_getchangelog) | action | Collection([ChangeLogParams](../Tipos-Complejos/ChangeLogParams.md)) | Get Change Log | Obtener registro de modificaciones |
| [`ChangeLogsService_GetChangeLogDifferences`](#changelogsservice_getchangelogdifferences) | action | Collection([ChangeLogDifferenceParams](../Tipos-Complejos/ChangeLogDifferenceParams.md)) | Get Change Log Differences | Obtener diferencias del registro de modificaciones |

## ChangeLogsService_GetChangeLog

- **Descripción (ES):** Obtener registro de modificaciones
- **Request:** `POST /b1s/v2/ChangeLogsService_GetChangeLog`
- **Parameters:** `GetChangeLogParams` ([GetChangeLogParams](../Tipos-Complejos/GetChangeLogParams.md))
- **Returns:** Collection([ChangeLogParams](../Tipos-Complejos/ChangeLogParams.md))

```json
{
  "GetChangeLogParams": {
    "PrimaryKey": "string",
    "UDOObjectCode": "string",
    ...
  }
}
```

## ChangeLogsService_GetChangeLogDifferences

- **Descripción (ES):** Obtener diferencias del registro de modificaciones
- **Request:** `POST /b1s/v2/ChangeLogsService_GetChangeLogDifferences`
- **Parameters:** `ShowDifferenceParams` ([ShowDifferenceParams](../Tipos-Complejos/ShowDifferenceParams.md))
- **Returns:** Collection([ChangeLogDifferenceParams](../Tipos-Complejos/ChangeLogDifferenceParams.md))

```json
{
  "ShowDifferenceParams": {
    "PrimaryKey": "string",
    "UDOObjectCode": "string",
    "LogInstance2": 0,
    "LogInstance": 0,
    ...
  }
}
```

