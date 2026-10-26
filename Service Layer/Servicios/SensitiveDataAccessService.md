# SensitiveDataAccessService — Servicio de acceso a datos sensibles

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `SensitiveDataAccessService`
- **Descripción (ES):** Servicio de acceso a datos sensibles
- **Operations:** 2

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`SensitiveDataAccessService_Access`](#sensitivedataaccessservice_access) | action | [SensitiveDataAccess](../Tipos-Complejos/SensitiveDataAccess.md) | Access | Registrar acceso |
| [`SensitiveDataAccessService_IsDataSensitive`](#sensitivedataaccessservice_isdatasensitive) | action | [DataSensitiveStatus](../Tipos-Complejos/DataSensitiveStatus.md) | Is Data Sensitive | Verificar si los datos son sensibles |

## SensitiveDataAccessService_Access

- **Descripción (ES):** Registrar acceso
- **Request:** `POST /b1s/v2/SensitiveDataAccessService_Access`
- **Parameters:** `SensitiveDataAccess` ([SensitiveDataAccess](../Tipos-Complejos/SensitiveDataAccess.md))
- **Returns:** [SensitiveDataAccess](../Tipos-Complejos/SensitiveDataAccess.md)

```json
{
  "SensitiveDataAccess": {
    "Table": "string",
    "Key1": "string",
    "Key2": "string",
    "Key3": "string",
    ...
  }
}
```

## SensitiveDataAccessService_IsDataSensitive

- **Descripción (ES):** Verificar si los datos son sensibles
- **Request:** `POST /b1s/v2/SensitiveDataAccessService_IsDataSensitive`
- **Parameters:** `SensitiveDataAccess` ([SensitiveDataAccess](../Tipos-Complejos/SensitiveDataAccess.md))
- **Returns:** [DataSensitiveStatus](../Tipos-Complejos/DataSensitiveStatus.md)

```json
{
  "SensitiveDataAccess": {
    "Table": "string",
    "Key1": "string",
    "Key2": "string",
    "Key3": "string",
    ...
  }
}
```

