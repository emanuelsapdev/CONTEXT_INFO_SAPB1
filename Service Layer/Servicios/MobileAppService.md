# MobileAppService — Servicio de apps móviles

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `MobileAppService`
- **Descripción (ES):** Servicio de apps móviles
- **Operations:** 14

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`MobileAppService_GetCurrentServerDateTime`](#mobileappservice_getcurrentserverdatetime) | action | [MobileServerDateTime](../Tipos-Complejos/MobileServerDateTime.md) | Get Current Server Date Time | Obtener fecha y hora actual del servidor |
| [`MobileAppService_GetDppChangeParams`](#mobileappservice_getdppchangeparams) | action | [DppChangeParams](../Tipos-Complejos/DppChangeParams.md) | Get Dpp Change Parameters | Obtener parámetros de cambio de protección de datos |
| [`MobileAppService_GetEmployeeFullNames`](#mobileappservice_getemployeefullnames) | action | Collection([EmployeeFullNamesParams](../Tipos-Complejos/EmployeeFullNamesParams.md)) | Get Employee Full Names | Obtener nombres completos de empleados |
| [`MobileAppService_GetSalesAppSetting`](#mobileappservice_getsalesappsetting) | action | [SalesAppSetting](../Tipos-Complejos/SalesAppSetting.md) | Get Sales App Setting | Obtener configuración de la app de ventas |
| [`MobileAppService_GetServiceAppReport`](#mobileappservice_getserviceappreport) | action | [ServiceAppReport](../Tipos-Complejos/ServiceAppReport.md) | Get Service App Report | Obtener informe de la app de servicio |
| [`MobileAppService_GetServiceAppReportContent`](#mobileappservice_getserviceappreportcontent) | action | [ServiceAppReportContent](../Tipos-Complejos/ServiceAppReportContent.md) | Get Service App Report Content | Obtener contenido del informe de la app de servicio |
| [`MobileAppService_GetTechnicianSchedulings`](#mobileappservice_gettechnicianschedulings) | action | Collection([TechnicianSchedulings](../Tipos-Complejos/TechnicianSchedulings.md)) | Get Technician Schedulings | Obtener programaciones de técnicos |
| [`MobileAppService_GetTechnicianSettings`](#mobileappservice_gettechniciansettings) | action | [TechnicianSettings](../Tipos-Complejos/TechnicianSettings.md) | Get Technician Settings | Obtener configuración de técnicos |
| [`MobileAppService_GetTechnicianSettingsGroup`](#mobileappservice_gettechniciansettingsgroup) | action | [TechnicianSettingsGroup](../Tipos-Complejos/TechnicianSettingsGroup.md) | Get Technician Settings Group | Obtener grupo de configuración de técnicos |
| [`MobileAppService_UpdateSalesAppSetting`](#mobileappservice_updatesalesappsetting) | action | — | Update Sales App Setting | Actualizar configuración de la app de ventas |
| [`MobileAppService_UpdateServiceAppReport`](#mobileappservice_updateserviceappreport) | action | — | Update Service App Report | Actualizar informe de la app de servicio |
| [`MobileAppService_UpdateServiceAppReportContent`](#mobileappservice_updateserviceappreportcontent) | action | — | Update Service App Report Content | Actualizar contenido del informe de la app de servicio |
| [`MobileAppService_UpdateTechnicianSettings`](#mobileappservice_updatetechniciansettings) | action | — | Update Technician Settings | Actualizar configuración de técnicos |
| [`MobileAppService_UpdateTechnicianSettingsGroup`](#mobileappservice_updatetechniciansettingsgroup) | action | — | Update Technician Settings Group | Actualizar grupo de configuración de técnicos |

## MobileAppService_GetCurrentServerDateTime

- **Descripción (ES):** Obtener fecha y hora actual del servidor
- **Request:** `POST /b1s/v2/MobileAppService_GetCurrentServerDateTime`
- **Parameters:** none
- **Returns:** [MobileServerDateTime](../Tipos-Complejos/MobileServerDateTime.md)

## MobileAppService_GetDppChangeParams

- **Descripción (ES):** Obtener parámetros de cambio de protección de datos
- **Request:** `POST /b1s/v2/MobileAppService_GetDppChangeParams`
- **Parameters:** `DppChangeParams` ([DppChangeParams](../Tipos-Complejos/DppChangeParams.md))
- **Returns:** [DppChangeParams](../Tipos-Complejos/DppChangeParams.md)

```json
{
  "DppChangeParams": {
    "FromDate": "2026-01-31",
    "FromTime": "12:00:00",
    ...
  }
}
```

## MobileAppService_GetEmployeeFullNames

- **Descripción (ES):** Obtener nombres completos de empleados
- **Request:** `POST /b1s/v2/MobileAppService_GetEmployeeFullNames`
- **Parameters:** `EmployeeFullNamesParamsCollection` (Collection([EmployeeFullNamesParams](../Tipos-Complejos/EmployeeFullNamesParams.md)))
- **Returns:** Collection([EmployeeFullNamesParams](../Tipos-Complejos/EmployeeFullNamesParams.md))

```json
{
  "EmployeeFullNamesParamsCollection": [ {
    "EmployeeID": 0,
    "EmployeeFullName": "string"
  } ]
}
```

## MobileAppService_GetSalesAppSetting

- **Descripción (ES):** Obtener configuración de la app de ventas
- **Request:** `POST /b1s/v2/MobileAppService_GetSalesAppSetting`
- **Parameters:** `SalesAppSettingParams` ([SalesAppSettingParams](../Tipos-Complejos/SalesAppSettingParams.md))
- **Returns:** [SalesAppSetting](../Tipos-Complejos/SalesAppSetting.md)

```json
{
  "SalesAppSettingParams": {
    "Code": 0,
    "Name": "string"
  }
}
```

## MobileAppService_GetServiceAppReport

- **Descripción (ES):** Obtener informe de la app de servicio
- **Request:** `POST /b1s/v2/MobileAppService_GetServiceAppReport`
- **Parameters:** `ServiceAppReportParams` ([ServiceAppReportParams](../Tipos-Complejos/ServiceAppReportParams.md))
- **Returns:** [ServiceAppReport](../Tipos-Complejos/ServiceAppReport.md)

```json
{
  "ServiceAppReportParams": {
    "Code": 0,
    ...
  }
}
```

## MobileAppService_GetServiceAppReportContent

- **Descripción (ES):** Obtener contenido del informe de la app de servicio
- **Request:** `POST /b1s/v2/MobileAppService_GetServiceAppReportContent`
- **Parameters:** `ServiceAppReportParams` ([ServiceAppReportParams](../Tipos-Complejos/ServiceAppReportParams.md))
- **Returns:** [ServiceAppReportContent](../Tipos-Complejos/ServiceAppReportContent.md)

```json
{
  "ServiceAppReportParams": {
    "Code": 0,
    ...
  }
}
```

## MobileAppService_GetTechnicianSchedulings

- **Descripción (ES):** Obtener programaciones de técnicos
- **Request:** `POST /b1s/v2/MobileAppService_GetTechnicianSchedulings`
- **Parameters:** `TechnicianSchedulingsParams` ([TechnicianSchedulingsParams](../Tipos-Complejos/TechnicianSchedulingsParams.md))
- **Returns:** Collection([TechnicianSchedulings](../Tipos-Complejos/TechnicianSchedulings.md))

```json
{
  "TechnicianSchedulingsParams": {
    "Technician": 0,
    "StartDate": "2026-01-31",
    "EndDate": "2026-01-31"
  }
}
```

## MobileAppService_GetTechnicianSettings

- **Descripción (ES):** Obtener configuración de técnicos
- **Request:** `POST /b1s/v2/MobileAppService_GetTechnicianSettings`
- **Parameters:** `TechnicianSettingsParams` ([TechnicianSettingsParams](../Tipos-Complejos/TechnicianSettingsParams.md))
- **Returns:** [TechnicianSettings](../Tipos-Complejos/TechnicianSettings.md)

```json
{
  "TechnicianSettingsParams": {
    "Technician": 0
  }
}
```

## MobileAppService_GetTechnicianSettingsGroup

- **Descripción (ES):** Obtener grupo de configuración de técnicos
- **Request:** `POST /b1s/v2/MobileAppService_GetTechnicianSettingsGroup`
- **Parameters:** `TechnicianSettingsGroupParams` ([TechnicianSettingsGroupParams](../Tipos-Complejos/TechnicianSettingsGroupParams.md))
- **Returns:** [TechnicianSettingsGroup](../Tipos-Complejos/TechnicianSettingsGroup.md)

```json
{
  "TechnicianSettingsGroupParams": {
    "Code": 0,
    "Name": "string"
  }
}
```

## MobileAppService_UpdateSalesAppSetting

- **Descripción (ES):** Actualizar configuración de la app de ventas
- **Request:** `POST /b1s/v2/MobileAppService_UpdateSalesAppSetting`
- **Parameters:** `SalesAppSetting` ([SalesAppSetting](../Tipos-Complejos/SalesAppSetting.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "SalesAppSetting": {
    "Code": 0,
    "Name": "string",
    "AdvancedDashBoard": 0,
    "CustomerAdvancedDashBoard": 0
  }
}
```

## MobileAppService_UpdateServiceAppReport

- **Descripción (ES):** Actualizar informe de la app de servicio
- **Request:** `POST /b1s/v2/MobileAppService_UpdateServiceAppReport`
- **Parameters:** `ServiceAppReport` ([ServiceAppReport](../Tipos-Complejos/ServiceAppReport.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "ServiceAppReport": {
    "Code": 0,
    "SystemReportName": "string",
    "CustomizedReportName": "string",
    ...
  }
}
```

## MobileAppService_UpdateServiceAppReportContent

- **Descripción (ES):** Actualizar contenido del informe de la app de servicio
- **Request:** `POST /b1s/v2/MobileAppService_UpdateServiceAppReportContent`
- **Parameters:** `ServiceAppReportParams` ([ServiceAppReportParams](../Tipos-Complejos/ServiceAppReportParams.md)), `ServiceAppReportContent` ([ServiceAppReportContent](../Tipos-Complejos/ServiceAppReportContent.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "ServiceAppReportParams": {
    "Code": 0,
    ...
  },
  "ServiceAppReportContent": {
    "ReportContent": "string"
  }
}
```

## MobileAppService_UpdateTechnicianSettings

- **Descripción (ES):** Actualizar configuración de técnicos
- **Request:** `POST /b1s/v2/MobileAppService_UpdateTechnicianSettings`
- **Parameters:** `TechnicianSettings` ([TechnicianSettings](../Tipos-Complejos/TechnicianSettings.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "TechnicianSettings": {
    "Technician": 0,
    "GroupCode": 0
  }
}
```

## MobileAppService_UpdateTechnicianSettingsGroup

- **Descripción (ES):** Actualizar grupo de configuración de técnicos
- **Request:** `POST /b1s/v2/MobileAppService_UpdateTechnicianSettingsGroup`
- **Parameters:** `TechnicianSettingsGroup` ([TechnicianSettingsGroup](../Tipos-Complejos/TechnicianSettingsGroup.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "TechnicianSettingsGroup": {
    "Code": 0,
    "Name": "string",
    "AdvancedDashBoard": 0,
    ...
  }
}
```

