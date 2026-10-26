# ElectronicDocumentService — Servicio de documentos electrónicos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `ElectronicDocumentService`
- **Descripción (ES):** Servicio de documentos electrónicos
- **Operations:** 17

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`ElectronicDocumentService_AddEmergencyNumber`](#electronicdocumentservice_addemergencynumber) | action | — | Add Emergency Number | Agregar número de emergencia |
| [`ElectronicDocumentService_AddImportEntry`](#electronicdocumentservice_addimportentry) | action | — | Add Import Entry | Agregar entrada de importación |
| [`ElectronicDocumentService_AddLog`](#electronicdocumentservice_addlog) | action | — | Add Log | Agregar registro |
| [`ElectronicDocumentService_CreateEntry`](#electronicdocumentservice_createentry) | action | — | Create Entry | Crear entrada |
| [`ElectronicDocumentService_ExportEntryLog`](#electronicdocumentservice_exportentrylog) | action | — | Export Entry Log | Exportar registro de entradas |
| [`ElectronicDocumentService_GetDocMappingList`](#electronicdocumentservice_getdocmappinglist) | action | Collection([EDFDocMapping](../Tipos-Complejos/EDFDocMapping.md)) | Get Document Mapping List | Obtener lista de mapeo de documentos |
| [`ElectronicDocumentService_GetEmergencyNumbers`](#electronicdocumentservice_getemergencynumbers) | action | Collection([EmergencyNumber](../Tipos-Complejos/EmergencyNumber.md)) | Get Emergency Numbers | Obtener números de emergencia |
| [`ElectronicDocumentService_GetEntry`](#electronicdocumentservice_getentry) | action | [EDFEntry](../Tipos-Complejos/EDFEntry.md) | Get Entry | Obtener entrada |
| [`ElectronicDocumentService_GetEntryList`](#electronicdocumentservice_getentrylist) | action | Collection([EDFEntry](../Tipos-Complejos/EDFEntry.md)) | Get Entry List | Obtener lista de entradas |
| [`ElectronicDocumentService_GetLastLog`](#electronicdocumentservice_getlastlog) | action | [EDFEntryLog](../Tipos-Complejos/EDFEntryLog.md) | Get Last Log | Obtener último registro |
| [`ElectronicDocumentService_GetLogs`](#electronicdocumentservice_getlogs) | action | Collection([EDFEntryLog](../Tipos-Complejos/EDFEntryLog.md)) | Get Logs | Obtener registros |
| [`ElectronicDocumentService_GetMappingByHash`](#electronicdocumentservice_getmappingbyhash) | action | [EDFMapping](../Tipos-Complejos/EDFMapping.md) | Get Mapping By Hash | Obtener mapeo por hash |
| [`ElectronicDocumentService_GetProtocolParameter`](#electronicdocumentservice_getprotocolparameter) | action | [EDFProtocolParameter](../Tipos-Complejos/EDFProtocolParameter.md) | Get Protocol Parameter | Obtener parámetro de protocolo |
| [`ElectronicDocumentService_GetProtocols`](#electronicdocumentservice_getprotocols) | function | Collection([EDFProtocol](../Entidades/ElectronicDocuments.md)) | Get Protocols | Obtener protocolos |
| [`ElectronicDocumentService_UpdateEntry`](#electronicdocumentservice_updateentry) | action | — | Update Entry | Actualizar entrada |
| [`ElectronicDocumentService_UpdateExtendedProperties`](#electronicdocumentservice_updateextendedproperties) | action | — | Update Extended Properties | Actualizar propiedades ampliadas |
| [`ElectronicDocumentService_UpdateProtocolParameter`](#electronicdocumentservice_updateprotocolparameter) | action | — | Update Protocol Parameter | Actualizar parámetro de protocolo |

## ElectronicDocumentService_AddEmergencyNumber

- **Descripción (ES):** Agregar número de emergencia
- **Request:** `POST /b1s/v2/ElectronicDocumentService_AddEmergencyNumber`
- **Parameters:** `EmergencyNumber` ([EmergencyNumber](../Tipos-Complejos/EmergencyNumber.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "EmergencyNumber": {
    "AbsEntry": 0,
    "Number": "string",
    "Code": "string",
    "Status": "string"
  }
}
```

## ElectronicDocumentService_AddImportEntry

- **Descripción (ES):** Agregar entrada de importación
- **Request:** `POST /b1s/v2/ElectronicDocumentService_AddImportEntry`
- **Parameters:** `EDFImportEntry` ([EDFImportEntry](../Tipos-Complejos/EDFImportEntry.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "EDFImportEntry": {
    "AbsEntry": 0,
    "Message": "string",
    "TestMode": "string",
    "GUID": "string",
    ...
  }
}
```

## ElectronicDocumentService_AddLog

- **Descripción (ES):** Agregar registro
- **Request:** `POST /b1s/v2/ElectronicDocumentService_AddLog`
- **Parameters:** `EDFEntryAddLogInputParams` ([EDFEntryAddLogInputParams](../Tipos-Complejos/EDFEntryAddLogInputParams.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "EDFEntryAddLogInputParams": {
    "GUID": "string",
    "LogMessage": "string",
    "LogData": "string",
    "ExportFormat": 0,
    ...
  }
}
```

## ElectronicDocumentService_CreateEntry

- **Descripción (ES):** Crear entrada
- **Request:** `POST /b1s/v2/ElectronicDocumentService_CreateEntry`
- **Parameters:** `EDFEntry` ([EDFEntry](../Tipos-Complejos/EDFEntry.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "EDFEntry": {
    "AbsEntry": 0,
    "ParentAbsEntry": 0,
    "BranchID": 0,
    "Environment": 0,
    ...
  }
}
```

## ElectronicDocumentService_ExportEntryLog

- **Descripción (ES):** Exportar registro de entradas
- **Request:** `POST /b1s/v2/ElectronicDocumentService_ExportEntryLog`
- **Parameters:** `EDFEntryLogInputParams` ([EDFEntryLogInputParams](../Tipos-Complejos/EDFEntryLogInputParams.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "EDFEntryLogInputParams": {
    "GUID": "string",
    "FileName": "string",
    ...
  }
}
```

## ElectronicDocumentService_GetDocMappingList

- **Descripción (ES):** Obtener lista de mapeo de documentos
- **Request:** `POST /b1s/v2/ElectronicDocumentService_GetDocMappingList`
- **Parameters:** `EDFDocMappingInputParams` ([EDFDocMappingInputParams](../Tipos-Complejos/EDFDocMappingInputParams.md))
- **Returns:** Collection([EDFDocMapping](../Tipos-Complejos/EDFDocMapping.md))

```json
{
  "EDFDocMappingInputParams": {
    "DocType": "string",
    ...
  }
}
```

## ElectronicDocumentService_GetEmergencyNumbers

- **Descripción (ES):** Obtener números de emergencia
- **Request:** `POST /b1s/v2/ElectronicDocumentService_GetEmergencyNumbers`
- **Parameters:** none
- **Returns:** Collection([EmergencyNumber](../Tipos-Complejos/EmergencyNumber.md))

## ElectronicDocumentService_GetEntry

- **Descripción (ES):** Obtener entrada
- **Request:** `POST /b1s/v2/ElectronicDocumentService_GetEntry`
- **Parameters:** `EDFEntryInputParams` ([EDFEntryInputParams](../Tipos-Complejos/EDFEntryInputParams.md))
- **Returns:** [EDFEntry](../Tipos-Complejos/EDFEntry.md)

```json
{
  "EDFEntryInputParams": {
    "GUID": "string",
    ...
  }
}
```

## ElectronicDocumentService_GetEntryList

- **Descripción (ES):** Obtener lista de entradas
- **Request:** `POST /b1s/v2/ElectronicDocumentService_GetEntryList`
- **Parameters:** `EDFEntryListInputParams` ([EDFEntryListInputParams](../Tipos-Complejos/EDFEntryListInputParams.md))
- **Returns:** Collection([EDFEntry](../Tipos-Complejos/EDFEntry.md))

```json
{
  "EDFEntryListInputParams": {
    "StoreEntryTypeSet": "string",
    "StoreEntryStatusSet": "string",
    "MaxLines": 0,
    "BranchID": 0,
    ...
  }
}
```

## ElectronicDocumentService_GetLastLog

- **Descripción (ES):** Obtener último registro
- **Request:** `POST /b1s/v2/ElectronicDocumentService_GetLastLog`
- **Parameters:** `EDFEntryLogInputParams` ([EDFEntryLogInputParams](../Tipos-Complejos/EDFEntryLogInputParams.md))
- **Returns:** [EDFEntryLog](../Tipos-Complejos/EDFEntryLog.md)

```json
{
  "EDFEntryLogInputParams": {
    "GUID": "string",
    "FileName": "string",
    ...
  }
}
```

## ElectronicDocumentService_GetLogs

- **Descripción (ES):** Obtener registros
- **Request:** `POST /b1s/v2/ElectronicDocumentService_GetLogs`
- **Parameters:** `EDFEntryLogInputParams` ([EDFEntryLogInputParams](../Tipos-Complejos/EDFEntryLogInputParams.md))
- **Returns:** Collection([EDFEntryLog](../Tipos-Complejos/EDFEntryLog.md))

```json
{
  "EDFEntryLogInputParams": {
    "GUID": "string",
    "FileName": "string",
    ...
  }
}
```

## ElectronicDocumentService_GetMappingByHash

- **Descripción (ES):** Obtener mapeo por hash
- **Request:** `POST /b1s/v2/ElectronicDocumentService_GetMappingByHash`
- **Parameters:** `EDFMappingInputParams` ([EDFMappingInputParams](../Tipos-Complejos/EDFMappingInputParams.md))
- **Returns:** [EDFMapping](../Tipos-Complejos/EDFMapping.md)

```json
{
  "EDFMappingInputParams": {
    "Hash": "string"
  }
}
```

## ElectronicDocumentService_GetProtocolParameter

- **Descripción (ES):** Obtener parámetro de protocolo
- **Request:** `POST /b1s/v2/ElectronicDocumentService_GetProtocolParameter`
- **Parameters:** `EDFProtocolParameterInputParams` ([EDFProtocolParameterInputParams](../Tipos-Complejos/EDFProtocolParameterInputParams.md))
- **Returns:** [EDFProtocolParameter](../Tipos-Complejos/EDFProtocolParameter.md)

```json
{
  "EDFProtocolParameterInputParams": {
    "LineNum": 0,
    "Branch": 0,
    ...
  }
}
```

## ElectronicDocumentService_GetProtocols

- **Descripción (ES):** Obtener protocolos
- **Request:** `GET /b1s/v2/ElectronicDocumentService_GetProtocols`
- **Parameters:** none
- **Returns:** Collection([EDFProtocol](../Entidades/ElectronicDocuments.md))

## ElectronicDocumentService_UpdateEntry

- **Descripción (ES):** Actualizar entrada
- **Request:** `POST /b1s/v2/ElectronicDocumentService_UpdateEntry`
- **Parameters:** `EDFEntry` ([EDFEntry](../Tipos-Complejos/EDFEntry.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "EDFEntry": {
    "AbsEntry": 0,
    "ParentAbsEntry": 0,
    "BranchID": 0,
    "Environment": 0,
    ...
  }
}
```

## ElectronicDocumentService_UpdateExtendedProperties

- **Descripción (ES):** Actualizar propiedades ampliadas
- **Request:** `POST /b1s/v2/ElectronicDocumentService_UpdateExtendedProperties`
- **Parameters:** `EDFProtocolWithParameters` ([EDFProtocolWithParameters](../Tipos-Complejos/EDFProtocolWithParameters.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "EDFProtocolWithParameters": {
    "Description": "string",
    ...
  }
}
```

## ElectronicDocumentService_UpdateProtocolParameter

- **Descripción (ES):** Actualizar parámetro de protocolo
- **Request:** `POST /b1s/v2/ElectronicDocumentService_UpdateProtocolParameter`
- **Parameters:** `EDFProtocolParameter` ([EDFProtocolParameter](../Tipos-Complejos/EDFProtocolParameter.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "EDFProtocolParameter": {
    "ParamName": "string",
    "ParamValue": "string",
    "ParameterID": 0,
    "BranchID": 0,
    ...
  }
}
```

