# ElectronicCommunicationActionsService — Servicio de acciones de comunicación electrónica

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `ElectronicCommunicationActionsService`
- **Descripción (ES):** Servicio de acciones de comunicación electrónica
- **Operations:** 8

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`ElectronicCommunicationActionsService_AddEcmAction`](#electroniccommunicationactionsservice_addecmaction) | action | [EcmAction](../Tipos-Complejos/EcmAction.md) | Add Ecm Action | Agregar acción de comunicación electrónica |
| [`ElectronicCommunicationActionsService_AddEcmActionLog`](#electroniccommunicationactionsservice_addecmactionlog) | action | [EcmActionLog](../Tipos-Complejos/EcmActionLog.md) | Add Ecm Action Log | Agregar registro de acción de comunicación electrónica |
| [`ElectronicCommunicationActionsService_DeleteEcmAction`](#electroniccommunicationactionsservice_deleteecmaction) | action | — | Delete Ecm Action | Eliminar acción de comunicación electrónica |
| [`ElectronicCommunicationActionsService_GetEcmAction`](#electroniccommunicationactionsservice_getecmaction) | action | [EcmAction](../Tipos-Complejos/EcmAction.md) | Get Ecm Action | Obtener acción de comunicación electrónica |
| [`ElectronicCommunicationActionsService_GetEcmActionByDoc`](#electroniccommunicationactionsservice_getecmactionbydoc) | action | [EcmAction](../Tipos-Complejos/EcmAction.md) | Get Ecm Action By Document | Obtener acción de comunicación electrónica por documento |
| [`ElectronicCommunicationActionsService_GetEcmActionLog`](#electroniccommunicationactionsservice_getecmactionlog) | action | [EcmActionLog](../Tipos-Complejos/EcmActionLog.md) | Get Ecm Action Log | Obtener registro de acción de comunicación electrónica |
| [`ElectronicCommunicationActionsService_GetEcmActionLogList`](#electroniccommunicationactionsservice_getecmactionloglist) | action | Collection([EcmActionLog](../Tipos-Complejos/EcmActionLog.md)) | Get Ecm Action Log List | Obtener lista de registros de acciones de comunicación electrónica |
| [`ElectronicCommunicationActionsService_UpdateEcmAction`](#electroniccommunicationactionsservice_updateecmaction) | action | — | Update Ecm Action | Actualizar acción de comunicación electrónica |

## ElectronicCommunicationActionsService_AddEcmAction

- **Descripción (ES):** Agregar acción de comunicación electrónica
- **Request:** `POST /b1s/v2/ElectronicCommunicationActionsService_AddEcmAction`
- **Parameters:** `EcmAction` ([EcmAction](../Tipos-Complejos/EcmAction.md))
- **Returns:** [EcmAction](../Tipos-Complejos/EcmAction.md)

```json
{
  "EcmAction": {
    "ActionID": 0,
    "Protocol": "string",
    "Description": "string",
    "Message": "string",
    ...
  }
}
```

## ElectronicCommunicationActionsService_AddEcmActionLog

- **Descripción (ES):** Agregar registro de acción de comunicación electrónica
- **Request:** `POST /b1s/v2/ElectronicCommunicationActionsService_AddEcmActionLog`
- **Parameters:** `EcmActionLog` ([EcmActionLog](../Tipos-Complejos/EcmActionLog.md))
- **Returns:** [EcmActionLog](../Tipos-Complejos/EcmActionLog.md)

```json
{
  "EcmActionLog": {
    "ActionID": 0,
    "LogID": 0,
    "Message": "string",
    "Data": "string",
    ...
  }
}
```

## ElectronicCommunicationActionsService_DeleteEcmAction

- **Descripción (ES):** Eliminar acción de comunicación electrónica
- **Request:** `POST /b1s/v2/ElectronicCommunicationActionsService_DeleteEcmAction`
- **Parameters:** `EcmAction` ([EcmAction](../Tipos-Complejos/EcmAction.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "EcmAction": {
    "ActionID": 0,
    "Protocol": "string",
    "Description": "string",
    "Message": "string",
    ...
  }
}
```

## ElectronicCommunicationActionsService_GetEcmAction

- **Descripción (ES):** Obtener acción de comunicación electrónica
- **Request:** `POST /b1s/v2/ElectronicCommunicationActionsService_GetEcmAction`
- **Parameters:** `EcmActionParams` ([EcmActionParams](../Tipos-Complejos/EcmActionParams.md))
- **Returns:** [EcmAction](../Tipos-Complejos/EcmAction.md)

```json
{
  "EcmActionParams": {
    "ActionID": 0
  }
}
```

## ElectronicCommunicationActionsService_GetEcmActionByDoc

- **Descripción (ES):** Obtener acción de comunicación electrónica por documento
- **Request:** `POST /b1s/v2/ElectronicCommunicationActionsService_GetEcmActionByDoc`
- **Parameters:** `EcmActionDocParams` ([EcmActionDocParams](../Tipos-Complejos/EcmActionDocParams.md))
- **Returns:** [EcmAction](../Tipos-Complejos/EcmAction.md)

```json
{
  "EcmActionDocParams": {
    "Protocol": "string",
    "SourceType": "string",
    "SourceObject": 0
  }
}
```

## ElectronicCommunicationActionsService_GetEcmActionLog

- **Descripción (ES):** Obtener registro de acción de comunicación electrónica
- **Request:** `POST /b1s/v2/ElectronicCommunicationActionsService_GetEcmActionLog`
- **Parameters:** `EcmActionLogParams` ([EcmActionLogParams](../Tipos-Complejos/EcmActionLogParams.md))
- **Returns:** [EcmActionLog](../Tipos-Complejos/EcmActionLog.md)

```json
{
  "EcmActionLogParams": {
    "ActionID": 0,
    "LogID": 0
  }
}
```

## ElectronicCommunicationActionsService_GetEcmActionLogList

- **Descripción (ES):** Obtener lista de registros de acciones de comunicación electrónica
- **Request:** `POST /b1s/v2/ElectronicCommunicationActionsService_GetEcmActionLogList`
- **Parameters:** `EcmAction` ([EcmAction](../Tipos-Complejos/EcmAction.md))
- **Returns:** Collection([EcmActionLog](../Tipos-Complejos/EcmActionLog.md))

```json
{
  "EcmAction": {
    "ActionID": 0,
    "Protocol": "string",
    "Description": "string",
    "Message": "string",
    ...
  }
}
```

## ElectronicCommunicationActionsService_UpdateEcmAction

- **Descripción (ES):** Actualizar acción de comunicación electrónica
- **Request:** `POST /b1s/v2/ElectronicCommunicationActionsService_UpdateEcmAction`
- **Parameters:** `EcmAction` ([EcmAction](../Tipos-Complejos/EcmAction.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "EcmAction": {
    "ActionID": 0,
    "Protocol": "string",
    "Description": "string",
    "Message": "string",
    ...
  }
}
```

