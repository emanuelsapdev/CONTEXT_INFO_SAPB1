# SeriesService — Servicio de series de numeración

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `SeriesService`
- **Descripción (ES):** Servicio de series de numeración
- **Operations:** 19

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`SeriesService_AddElectronicSeries`](#seriesservice_addelectronicseries) | action | [ElectronicSeriesParams](../Tipos-Complejos/ElectronicSeriesParams.md) | Add Electronic Series | Agregar serie electrónica |
| [`SeriesService_AddSeries`](#seriesservice_addseries) | action | [SeriesParams](../Tipos-Complejos/SeriesParams.md) | Add Series | Agregar serie |
| [`SeriesService_AttachSeriesToDocument`](#seriesservice_attachseriestodocument) | action | — | Attach Series To Document | Asignar serie a documento |
| [`SeriesService_ChangeDocumentMenuName`](#seriesservice_changedocumentmenuname) | action | — | Change Document Menu Name | Cambiar nombre de menú del documento |
| [`SeriesService_GetDefaultElectronicSeries`](#seriesservice_getdefaultelectronicseries) | action | [ElectronicSeriesParams](../Tipos-Complejos/ElectronicSeriesParams.md) | Get Default Electronic Series | Obtener serie electrónica predeterminada |
| [`SeriesService_GetDefaultSeries`](#seriesservice_getdefaultseries) | action | [Series](../Tipos-Complejos/Series.md) | Get Default Series | Obtener serie predeterminada |
| [`SeriesService_GetDocumentChangedMenuName`](#seriesservice_getdocumentchangedmenuname) | action | [DocumentChangeMenuName](../Tipos-Complejos/DocumentChangeMenuName.md) | Get Document Changed Menu Name | Obtener nombre de menú modificado del documento |
| [`SeriesService_GetDocumentSeries`](#seriesservice_getdocumentseries) | action | Collection([Series](../Tipos-Complejos/Series.md)) | Get Document Series | Obtener series del documento |
| [`SeriesService_GetElectronicSeries`](#seriesservice_getelectronicseries) | action | [ElectronicSeries](../Tipos-Complejos/ElectronicSeries.md) | Get Electronic Series | Obtener serie electrónica |
| [`SeriesService_GetSeries`](#seriesservice_getseries) | action | [Series](../Tipos-Complejos/Series.md) | Get Series | Obtener serie |
| [`SeriesService_RemoveElectronicSeries`](#seriesservice_removeelectronicseries) | action | — | Remove Electronic Series | Eliminar serie electrónica |
| [`SeriesService_RemoveSeries`](#seriesservice_removeseries) | action | — | Remove Series | Eliminar serie |
| [`SeriesService_SetDefaultElectronicSeries`](#seriesservice_setdefaultelectronicseries) | action | — | Set Default Electronic Series | Establecer serie electrónica predeterminada |
| [`SeriesService_SetDefaultSeriesForAllUsers`](#seriesservice_setdefaultseriesforallusers) | action | — | Set Default Series For All Users | Establecer serie predeterminada para todos los usuarios |
| [`SeriesService_SetDefaultSeriesForCurrentUser`](#seriesservice_setdefaultseriesforcurrentuser) | action | — | Set Default Series For Current User | Establecer serie predeterminada para el usuario actual |
| [`SeriesService_SetDefaultSeriesForUser`](#seriesservice_setdefaultseriesforuser) | action | — | Set Default Series For User | Establecer serie predeterminada para un usuario |
| [`SeriesService_UnattachSeriesFromDocument`](#seriesservice_unattachseriesfromdocument) | action | — | Unattach Series From Document | Desasignar serie del documento |
| [`SeriesService_UpdateElectronicSeries`](#seriesservice_updateelectronicseries) | action | — | Update Electronic Series | Actualizar serie electrónica |
| [`SeriesService_UpdateSeries`](#seriesservice_updateseries) | action | — | Update Series | Actualizar serie |

## SeriesService_AddElectronicSeries

- **Descripción (ES):** Agregar serie electrónica
- **Request:** `POST /b1s/v2/SeriesService_AddElectronicSeries`
- **Parameters:** `ElectronicSeries` ([ElectronicSeries](../Tipos-Complejos/ElectronicSeries.md))
- **Returns:** [ElectronicSeriesParams](../Tipos-Complejos/ElectronicSeriesParams.md)

```json
{
  "ElectronicSeries": {
    "ElectronicSeriesProperty": 0,
    "Series": 0,
    "Name": "string",
    "InitialNumber": "string",
    ...
  }
}
```

## SeriesService_AddSeries

- **Descripción (ES):** Agregar serie
- **Request:** `POST /b1s/v2/SeriesService_AddSeries`
- **Parameters:** `Series` ([Series](../Tipos-Complejos/Series.md))
- **Returns:** [SeriesParams](../Tipos-Complejos/SeriesParams.md)

```json
{
  "Series": {
    "Document": "string",
    "DocumentSubType": "string",
    "InitialNumber": 0,
    "LastNumber": 0,
    ...
  }
}
```

## SeriesService_AttachSeriesToDocument

- **Descripción (ES):** Asignar serie a documento
- **Request:** `POST /b1s/v2/SeriesService_AttachSeriesToDocument`
- **Parameters:** `DocumentSeriesParams` ([DocumentSeriesParams](../Tipos-Complejos/DocumentSeriesParams.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "DocumentSeriesParams": {
    "Document": "string",
    "DocumentSubType": "string",
    "Series": 0
  }
}
```

## SeriesService_ChangeDocumentMenuName

- **Descripción (ES):** Cambiar nombre de menú del documento
- **Request:** `POST /b1s/v2/SeriesService_ChangeDocumentMenuName`
- **Parameters:** `DocumentChangeMenuName` ([DocumentChangeMenuName](../Tipos-Complejos/DocumentChangeMenuName.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "DocumentChangeMenuName": {
    "Document": "string",
    "DocumentSubType": "string",
    "ChangedMenuName": "string"
  }
}
```

## SeriesService_GetDefaultElectronicSeries

- **Descripción (ES):** Obtener serie electrónica predeterminada
- **Request:** `POST /b1s/v2/SeriesService_GetDefaultElectronicSeries`
- **Parameters:** `SeriesParams` ([SeriesParams](../Tipos-Complejos/SeriesParams.md))
- **Returns:** [ElectronicSeriesParams](../Tipos-Complejos/ElectronicSeriesParams.md)

```json
{
  "SeriesParams": {
    "Series": 0
  }
}
```

## SeriesService_GetDefaultSeries

- **Descripción (ES):** Obtener serie predeterminada
- **Request:** `POST /b1s/v2/SeriesService_GetDefaultSeries`
- **Parameters:** `DocumentTypeParams` ([DocumentTypeParams](../Tipos-Complejos/DocumentTypeParams.md))
- **Returns:** [Series](../Tipos-Complejos/Series.md)

```json
{
  "DocumentTypeParams": {
    "Document": "string",
    "DocumentSubType": "string"
  }
}
```

## SeriesService_GetDocumentChangedMenuName

- **Descripción (ES):** Obtener nombre de menú modificado del documento
- **Request:** `POST /b1s/v2/SeriesService_GetDocumentChangedMenuName`
- **Parameters:** `DocumentTypeParams` ([DocumentTypeParams](../Tipos-Complejos/DocumentTypeParams.md))
- **Returns:** [DocumentChangeMenuName](../Tipos-Complejos/DocumentChangeMenuName.md)

```json
{
  "DocumentTypeParams": {
    "Document": "string",
    "DocumentSubType": "string"
  }
}
```

## SeriesService_GetDocumentSeries

- **Descripción (ES):** Obtener series del documento
- **Request:** `POST /b1s/v2/SeriesService_GetDocumentSeries`
- **Parameters:** `DocumentTypeParams` ([DocumentTypeParams](../Tipos-Complejos/DocumentTypeParams.md))
- **Returns:** Collection([Series](../Tipos-Complejos/Series.md))

```json
{
  "DocumentTypeParams": {
    "Document": "string",
    "DocumentSubType": "string"
  }
}
```

## SeriesService_GetElectronicSeries

- **Descripción (ES):** Obtener serie electrónica
- **Request:** `POST /b1s/v2/SeriesService_GetElectronicSeries`
- **Parameters:** `ElectronicSeriesParams` ([ElectronicSeriesParams](../Tipos-Complejos/ElectronicSeriesParams.md))
- **Returns:** [ElectronicSeries](../Tipos-Complejos/ElectronicSeries.md)

```json
{
  "ElectronicSeriesParams": {
    "ElectronicSeries": 0
  }
}
```

## SeriesService_GetSeries

- **Descripción (ES):** Obtener serie
- **Request:** `POST /b1s/v2/SeriesService_GetSeries`
- **Parameters:** `SeriesParams` ([SeriesParams](../Tipos-Complejos/SeriesParams.md))
- **Returns:** [Series](../Tipos-Complejos/Series.md)

```json
{
  "SeriesParams": {
    "Series": 0
  }
}
```

## SeriesService_RemoveElectronicSeries

- **Descripción (ES):** Eliminar serie electrónica
- **Request:** `POST /b1s/v2/SeriesService_RemoveElectronicSeries`
- **Parameters:** `ElectronicSeriesParams` ([ElectronicSeriesParams](../Tipos-Complejos/ElectronicSeriesParams.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "ElectronicSeriesParams": {
    "ElectronicSeries": 0
  }
}
```

## SeriesService_RemoveSeries

- **Descripción (ES):** Eliminar serie
- **Request:** `POST /b1s/v2/SeriesService_RemoveSeries`
- **Parameters:** `SeriesParams` ([SeriesParams](../Tipos-Complejos/SeriesParams.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "SeriesParams": {
    "Series": 0
  }
}
```

## SeriesService_SetDefaultElectronicSeries

- **Descripción (ES):** Establecer serie electrónica predeterminada
- **Request:** `POST /b1s/v2/SeriesService_SetDefaultElectronicSeries`
- **Parameters:** `DefaultElectronicSeriesParams` ([DefaultElectronicSeriesParams](../Tipos-Complejos/DefaultElectronicSeriesParams.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "DefaultElectronicSeriesParams": {
    "Series": 0,
    "ElectronicSeries": 0
  }
}
```

## SeriesService_SetDefaultSeriesForAllUsers

- **Descripción (ES):** Establecer serie predeterminada para todos los usuarios
- **Request:** `POST /b1s/v2/SeriesService_SetDefaultSeriesForAllUsers`
- **Parameters:** `DocumentSeriesParams` ([DocumentSeriesParams](../Tipos-Complejos/DocumentSeriesParams.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "DocumentSeriesParams": {
    "Document": "string",
    "DocumentSubType": "string",
    "Series": 0
  }
}
```

## SeriesService_SetDefaultSeriesForCurrentUser

- **Descripción (ES):** Establecer serie predeterminada para el usuario actual
- **Request:** `POST /b1s/v2/SeriesService_SetDefaultSeriesForCurrentUser`
- **Parameters:** `DocumentSeriesParams` ([DocumentSeriesParams](../Tipos-Complejos/DocumentSeriesParams.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "DocumentSeriesParams": {
    "Document": "string",
    "DocumentSubType": "string",
    "Series": 0
  }
}
```

## SeriesService_SetDefaultSeriesForUser

- **Descripción (ES):** Establecer serie predeterminada para un usuario
- **Request:** `POST /b1s/v2/SeriesService_SetDefaultSeriesForUser`
- **Parameters:** `DocumentSeriesUserParams` ([DocumentSeriesUserParams](../Tipos-Complejos/DocumentSeriesUserParams.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "DocumentSeriesUserParams": {
    "Document": "string",
    "DocumentSubType": "string",
    "Series": 0,
    "User": 0
  }
}
```

## SeriesService_UnattachSeriesFromDocument

- **Descripción (ES):** Desasignar serie del documento
- **Request:** `POST /b1s/v2/SeriesService_UnattachSeriesFromDocument`
- **Parameters:** `DocumentSeriesParams` ([DocumentSeriesParams](../Tipos-Complejos/DocumentSeriesParams.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "DocumentSeriesParams": {
    "Document": "string",
    "DocumentSubType": "string",
    "Series": 0
  }
}
```

## SeriesService_UpdateElectronicSeries

- **Descripción (ES):** Actualizar serie electrónica
- **Request:** `POST /b1s/v2/SeriesService_UpdateElectronicSeries`
- **Parameters:** `ElectronicSeries` ([ElectronicSeries](../Tipos-Complejos/ElectronicSeries.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "ElectronicSeries": {
    "ElectronicSeriesProperty": 0,
    "Series": 0,
    "Name": "string",
    "InitialNumber": "string",
    ...
  }
}
```

## SeriesService_UpdateSeries

- **Descripción (ES):** Actualizar serie
- **Request:** `POST /b1s/v2/SeriesService_UpdateSeries`
- **Parameters:** `Series` ([Series](../Tipos-Complejos/Series.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "Series": {
    "Document": "string",
    "DocumentSubType": "string",
    "InitialNumber": 0,
    "LastNumber": 0,
    ...
  }
}
```

