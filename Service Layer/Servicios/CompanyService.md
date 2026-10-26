# CompanyService — Servicio de la sociedad

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `CompanyService`
- **Descripción (ES):** Servicio de la sociedad
- **Operations:** 23

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`CompanyService_CreatePeriod`](#companyservice_createperiod) | action | [PeriodCategoryParams](../Tipos-Complejos/PeriodCategoryParams.md) | Create Period | Crear período |
| [`CompanyService_CreatePeriodWithFinanceParams`](#companyservice_createperiodwithfinanceparams) | action | [PeriodCategoryParams](../Tipos-Complejos/PeriodCategoryParams.md) | Create Period With Finance Parameters | Crear período con parámetros financieros |
| [`CompanyService_GetAdminInfo`](#companyservice_getadmininfo) | function | [AdminInfo](../Tipos-Complejos/AdminInfo.md) | Get Admin Information | Obtener datos de administración |
| [`CompanyService_GetAdvancedGLAccount`](#companyservice_getadvancedglaccount) | action | [AdvancedGLAccountReturnParams](../Tipos-Complejos/AdvancedGLAccountReturnParams.md) | Get Advanced G/L Account | Obtener cuenta de mayor avanzada (determinación) |
| [`CompanyService_GetCompanyInfo`](#companyservice_getcompanyinfo) | function | [CompanyInfo](../Tipos-Complejos/CompanyInfo.md) | Get Company Information | Obtener información de la sociedad |
| [`CompanyService_GetCurrentServerTime`](#companyservice_getcurrentservertime) | function | [CurrentServerTime](../Tipos-Complejos/CurrentServerTime.md) | Get Current Server Time | Obtener hora actual del servidor |
| [`CompanyService_GetFeaturesStatus`](#companyservice_getfeaturesstatus) | action | Collection([FeatureStatus](../Tipos-Complejos/FeatureStatus.md)) | Get Features Status | Obtener estado de funcionalidades |
| [`CompanyService_GetFinancePeriod`](#companyservice_getfinanceperiod) | action | [FinancePeriod](../Tipos-Complejos/FinancePeriod.md) | Get Finance Period | Obtener período contable |
| [`CompanyService_GetFinancePeriods`](#companyservice_getfinanceperiods) | action | Collection([FinancePeriod](../Tipos-Complejos/FinancePeriod.md)) | Get Finance Periods | Obtener períodos contables |
| [`CompanyService_GetItemPrice`](#companyservice_getitemprice) | action | [ItemPriceReturnParams](../Tipos-Complejos/ItemPriceReturnParams.md) | Get Item Price | Obtener precio del artículo |
| [`CompanyService_GetPathAdmin`](#companyservice_getpathadmin) | function | [PathAdmin](../Tipos-Complejos/PathAdmin.md) | Get Path Admin | Obtener rutas de administración |
| [`CompanyService_GetPeriod`](#companyservice_getperiod) | action | [PeriodCategory](../Tipos-Complejos/PeriodCategory.md) | Get Period | Obtener período |
| [`CompanyService_GetPeriods`](#companyservice_getperiods) | action | Collection([PeriodCategoryParams](../Tipos-Complejos/PeriodCategoryParams.md)) | Get Periods | Obtener períodos |
| [`CompanyService_LogLoginAction`](#companyservice_logloginaction) | action | [SupportUserLoginRecord](../Tipos-Complejos/SupportUserLoginRecord.md) | Log Login Action | Registrar acción de inicio de sesión |
| [`CompanyService_LogLogoffAction`](#companyservice_loglogoffaction) | action | — | Log Logoff Action | Registrar acción de cierre de sesión |
| [`CompanyService_RefreshPathsinDocuments`](#companyservice_refreshpathsindocuments) | action | [RefreshPathsDocuments](../Tipos-Complejos/RefreshPathsDocuments.md) | Refresh Pathsin Documents | Actualizar rutas en documentos |
| [`CompanyService_RemoveFinancePeriod`](#companyservice_removefinanceperiod) | action | — | Remove Finance Period | Eliminar período contable |
| [`CompanyService_RoundDecimal`](#companyservice_rounddecimal) | action | [RoundedData](../Tipos-Complejos/RoundedData.md) | Round Decimal | Redondear decimal |
| [`CompanyService_UpdateAdminInfo`](#companyservice_updateadmininfo) | action | — | Update Admin Information | Actualizar datos de administración |
| [`CompanyService_UpdateCompanyInfo`](#companyservice_updatecompanyinfo) | action | — | Update Company Information | Actualizar información de la sociedad |
| [`CompanyService_UpdateFinancePeriod`](#companyservice_updatefinanceperiod) | action | — | Update Finance Period | Actualizar período contable |
| [`CompanyService_UpdatePathAdmin`](#companyservice_updatepathadmin) | action | — | Update Path Admin | Actualizar rutas de administración |
| [`CompanyService_UpdatePeriod`](#companyservice_updateperiod) | action | — | Update Period | Actualizar período |

## CompanyService_CreatePeriod

- **Descripción (ES):** Crear período
- **Request:** `POST /b1s/v2/CompanyService_CreatePeriod`
- **Parameters:** `PeriodCategory` ([PeriodCategory](../Tipos-Complejos/PeriodCategory.md))
- **Returns:** [PeriodCategoryParams](../Tipos-Complejos/PeriodCategoryParams.md)

```json
{
  "PeriodCategory": {
    "AbsoluteEntry": 0,
    "BeginningofFinancialYear": "2026-01-31",
    "PeriodCategoryProperty": "string",
    "NumberOfPeriods": 0,
    ...
  }
}
```

## CompanyService_CreatePeriodWithFinanceParams

- **Descripción (ES):** Crear período con parámetros financieros
- **Request:** `POST /b1s/v2/CompanyService_CreatePeriodWithFinanceParams`
- **Parameters:** `PeriodCategory` ([PeriodCategory](../Tipos-Complejos/PeriodCategory.md)), `FinancePeriodParams` ([FinancePeriodParams](../Tipos-Complejos/FinancePeriodParams.md))
- **Returns:** [PeriodCategoryParams](../Tipos-Complejos/PeriodCategoryParams.md)

```json
{
  "PeriodCategory": {
    "AbsoluteEntry": 0,
    "BeginningofFinancialYear": "2026-01-31",
    "PeriodCategoryProperty": "string",
    "NumberOfPeriods": 0,
    ...
  },
  "FinancePeriodParams": {
    "AbsoluteEntry": 0,
    "PeriodIndicator": "string"
  }
}
```

## CompanyService_GetAdminInfo

- **Descripción (ES):** Obtener datos de administración
- **Request:** `GET /b1s/v2/CompanyService_GetAdminInfo`
- **Parameters:** none
- **Returns:** [AdminInfo](../Tipos-Complejos/AdminInfo.md)

## CompanyService_GetAdvancedGLAccount

- **Descripción (ES):** Obtener cuenta de mayor avanzada (determinación)
- **Request:** `POST /b1s/v2/CompanyService_GetAdvancedGLAccount`
- **Parameters:** `AdvancedGLAccountParams` ([AdvancedGLAccountParams](../Tipos-Complejos/AdvancedGLAccountParams.md))
- **Returns:** [AdvancedGLAccountReturnParams](../Tipos-Complejos/AdvancedGLAccountReturnParams.md)

```json
{
  "AdvancedGLAccountParams": {
    "ItemCode": "string",
    "Warehouse": "string",
    "BPCode": "string",
    "FederalTaxID": "string",
    ...
  }
}
```

## CompanyService_GetCompanyInfo

- **Descripción (ES):** Obtener información de la sociedad
- **Request:** `GET /b1s/v2/CompanyService_GetCompanyInfo`
- **Parameters:** none
- **Returns:** [CompanyInfo](../Tipos-Complejos/CompanyInfo.md)

## CompanyService_GetCurrentServerTime

- **Descripción (ES):** Obtener hora actual del servidor
- **Request:** `GET /b1s/v2/CompanyService_GetCurrentServerTime`
- **Parameters:** none
- **Returns:** [CurrentServerTime](../Tipos-Complejos/CurrentServerTime.md)

## CompanyService_GetFeaturesStatus

- **Descripción (ES):** Obtener estado de funcionalidades
- **Request:** `POST /b1s/v2/CompanyService_GetFeaturesStatus`
- **Parameters:** none
- **Returns:** Collection([FeatureStatus](../Tipos-Complejos/FeatureStatus.md))

## CompanyService_GetFinancePeriod

- **Descripción (ES):** Obtener período contable
- **Request:** `POST /b1s/v2/CompanyService_GetFinancePeriod`
- **Parameters:** `FinancePeriodParams` ([FinancePeriodParams](../Tipos-Complejos/FinancePeriodParams.md))
- **Returns:** [FinancePeriod](../Tipos-Complejos/FinancePeriod.md)

```json
{
  "FinancePeriodParams": {
    "AbsoluteEntry": 0,
    "PeriodIndicator": "string"
  }
}
```

## CompanyService_GetFinancePeriods

- **Descripción (ES):** Obtener períodos contables
- **Request:** `POST /b1s/v2/CompanyService_GetFinancePeriods`
- **Parameters:** `PeriodCategoryParams` ([PeriodCategoryParams](../Tipos-Complejos/PeriodCategoryParams.md))
- **Returns:** Collection([FinancePeriod](../Tipos-Complejos/FinancePeriod.md))

```json
{
  "PeriodCategoryParams": {
    "AbsoluteEntry": 0
  }
}
```

## CompanyService_GetItemPrice

- **Descripción (ES):** Obtener precio del artículo
- **Request:** `POST /b1s/v2/CompanyService_GetItemPrice`
- **Parameters:** `ItemPriceParams` ([ItemPriceParams](../Tipos-Complejos/ItemPriceParams.md))
- **Returns:** [ItemPriceReturnParams](../Tipos-Complejos/ItemPriceReturnParams.md)

```json
{
  "ItemPriceParams": {
    "Date": "2026-01-31",
    "UoMEntry": 0,
    "BlanketAgreementNumber": 0,
    "BlanketAgreementLine": 0,
    ...
  }
}
```

## CompanyService_GetPathAdmin

- **Descripción (ES):** Obtener rutas de administración
- **Request:** `GET /b1s/v2/CompanyService_GetPathAdmin`
- **Parameters:** none
- **Returns:** [PathAdmin](../Tipos-Complejos/PathAdmin.md)

## CompanyService_GetPeriod

- **Descripción (ES):** Obtener período
- **Request:** `POST /b1s/v2/CompanyService_GetPeriod`
- **Parameters:** `PeriodCategoryParams` ([PeriodCategoryParams](../Tipos-Complejos/PeriodCategoryParams.md))
- **Returns:** [PeriodCategory](../Tipos-Complejos/PeriodCategory.md)

```json
{
  "PeriodCategoryParams": {
    "AbsoluteEntry": 0
  }
}
```

## CompanyService_GetPeriods

- **Descripción (ES):** Obtener períodos
- **Request:** `POST /b1s/v2/CompanyService_GetPeriods`
- **Parameters:** none
- **Returns:** Collection([PeriodCategoryParams](../Tipos-Complejos/PeriodCategoryParams.md))

## CompanyService_LogLoginAction

- **Descripción (ES):** Registrar acción de inicio de sesión
- **Request:** `POST /b1s/v2/CompanyService_LogLoginAction`
- **Parameters:** `UserAccessLog` ([UserAccessLog](../Tipos-Complejos/UserAccessLog.md)), `SupportUserLoginRecord` ([SupportUserLoginRecord](../Tipos-Complejos/SupportUserLoginRecord.md))
- **Returns:** [SupportUserLoginRecord](../Tipos-Complejos/SupportUserLoginRecord.md)

```json
{
  "UserAccessLog": {
    "UserCode": "string",
    "ActionBy": "string",
    "ClientIP": "string",
    "ClientName": "string",
    ...
  },
  "SupportUserLoginRecord": {
    "ID": 0,
    "RealName": "string",
    "LogDetail": "string",
    ...
  }
}
```

## CompanyService_LogLogoffAction

- **Descripción (ES):** Registrar acción de cierre de sesión
- **Request:** `POST /b1s/v2/CompanyService_LogLogoffAction`
- **Parameters:** `UserAccessLog` ([UserAccessLog](../Tipos-Complejos/UserAccessLog.md)), `SupportUserLoginRecord` ([SupportUserLoginRecord](../Tipos-Complejos/SupportUserLoginRecord.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "UserAccessLog": {
    "UserCode": "string",
    "ActionBy": "string",
    "ClientIP": "string",
    "ClientName": "string",
    ...
  },
  "SupportUserLoginRecord": {
    "ID": 0,
    "RealName": "string",
    "LogDetail": "string",
    ...
  }
}
```

## CompanyService_RefreshPathsinDocuments

- **Descripción (ES):** Actualizar rutas en documentos
- **Request:** `POST /b1s/v2/CompanyService_RefreshPathsinDocuments`
- **Parameters:** none
- **Returns:** [RefreshPathsDocuments](../Tipos-Complejos/RefreshPathsDocuments.md)

## CompanyService_RemoveFinancePeriod

- **Descripción (ES):** Eliminar período contable
- **Request:** `POST /b1s/v2/CompanyService_RemoveFinancePeriod`
- **Parameters:** `FinancePeriodParams` ([FinancePeriodParams](../Tipos-Complejos/FinancePeriodParams.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "FinancePeriodParams": {
    "AbsoluteEntry": 0,
    "PeriodIndicator": "string"
  }
}
```

## CompanyService_RoundDecimal

- **Descripción (ES):** Redondear decimal
- **Request:** `POST /b1s/v2/CompanyService_RoundDecimal`
- **Parameters:** `DecimalData` ([DecimalData](../Tipos-Complejos/DecimalData.md))
- **Returns:** [RoundedData](../Tipos-Complejos/RoundedData.md)

```json
{
  "DecimalData": {
    "Value": 0.0,
    "Currency": "string",
    ...
  }
}
```

## CompanyService_UpdateAdminInfo

- **Descripción (ES):** Actualizar datos de administración
- **Request:** `POST /b1s/v2/CompanyService_UpdateAdminInfo`
- **Parameters:** `AdminInfo` ([AdminInfo](../Tipos-Complejos/AdminInfo.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "AdminInfo": {
    "Code": 0,
    "CompanyName": "string",
    "Address": "string",
    "Country": "string",
    ...
  }
}
```

## CompanyService_UpdateCompanyInfo

- **Descripción (ES):** Actualizar información de la sociedad
- **Request:** `POST /b1s/v2/CompanyService_UpdateCompanyInfo`
- **Parameters:** `CompanyInfo` ([CompanyInfo](../Tipos-Complejos/CompanyInfo.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "CompanyInfo": {
    "Version": 0,
    "BISRBankActKey": 0,
    "BISRBankCountry": "string",
    "BISRBankNo": "string",
    ...
  }
}
```

## CompanyService_UpdateFinancePeriod

- **Descripción (ES):** Actualizar período contable
- **Request:** `POST /b1s/v2/CompanyService_UpdateFinancePeriod`
- **Parameters:** `FinancePeriod` ([FinancePeriod](../Tipos-Complejos/FinancePeriod.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "FinancePeriod": {
    "AbsoluteEntry": 0,
    "PeriodCode": "string",
    "PeriodName": "string",
    "PostingDateFrom": "2026-01-31",
    ...
  }
}
```

## CompanyService_UpdatePathAdmin

- **Descripción (ES):** Actualizar rutas de administración
- **Request:** `POST /b1s/v2/CompanyService_UpdatePathAdmin`
- **Parameters:** `PathAdmin` ([PathAdmin](../Tipos-Complejos/PathAdmin.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "PathAdmin": {
    "WordTemplateFolderPath": "string",
    "PicturesFolderPath": "string",
    "AttachmentsFolderPath": "string",
    "ExtensionsFolderPath": "string",
    ...
  }
}
```

## CompanyService_UpdatePeriod

- **Descripción (ES):** Actualizar período
- **Request:** `POST /b1s/v2/CompanyService_UpdatePeriod`
- **Parameters:** `PeriodCategory` ([PeriodCategory](../Tipos-Complejos/PeriodCategory.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "PeriodCategory": {
    "AbsoluteEntry": 0,
    "BeginningofFinancialYear": "2026-01-31",
    "PeriodCategoryProperty": "string",
    "NumberOfPeriods": 0,
    ...
  }
}
```

