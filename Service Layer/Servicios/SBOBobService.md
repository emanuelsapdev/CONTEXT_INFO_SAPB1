# SBOBobService — Servicio SBOBob (utilidades del sistema)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `SBOBobService`
- **Descripción (ES):** Servicio SBOBob (utilidades del sistema)
- **Operations:** 9

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`SBOBobService_Format_MoneyToString`](#sbobobservice_format_moneytostring) | function | Edm.String | Format Money To String | Formatear importe a texto |
| [`SBOBobService_GetCurrencyRate`](#sbobobservice_getcurrencyrate) | function | Edm.Double | Get Currency Rate | Obtener tipo de cambio |
| [`SBOBobService_GetDueDate`](#sbobobservice_getduedate) | function | Edm.String | Get Due Date | Obtener fecha de vencimiento |
| [`SBOBobService_GetIndexRate`](#sbobobservice_getindexrate) | function | Edm.Double | Get Index Rate | Obtener tasa del índice |
| [`SBOBobService_GetLocalCurrency`](#sbobobservice_getlocalcurrency) | function | Edm.String | Get Local Currency | Obtener moneda local |
| [`SBOBobService_GetSystemCurrency`](#sbobobservice_getsystemcurrency) | function | Edm.String | Get System Currency | Obtener moneda del sistema |
| [`SBOBobService_GetSystemPermission`](#sbobobservice_getsystempermission) | function | Edm.Int32 | Get System Permission | Obtener permiso del sistema |
| [`SBOBobService_SetCurrencyRate`](#sbobobservice_setcurrencyrate) | action | — | Set Currency Rate | Establecer tipo de cambio |
| [`SBOBobService_SetSystemPermission`](#sbobobservice_setsystempermission) | action | — | Set System Permission | Establecer permiso del sistema |

## SBOBobService_Format_MoneyToString

- **Descripción (ES):** Formatear importe a texto
- **Request:** `GET /b1s/v2/SBOBobService_Format_MoneyToString`
- **Parameters:** `InMoney` (Edm.Double), `InPrecision` (Edm.String)
- **Returns:** Edm.String

## SBOBobService_GetCurrencyRate

- **Descripción (ES):** Obtener tipo de cambio
- **Request:** `GET /b1s/v2/SBOBobService_GetCurrencyRate`
- **Parameters:** `Currency` (Edm.String), `Date` (Edm.String)
- **Returns:** Edm.Double

## SBOBobService_GetDueDate

- **Descripción (ES):** Obtener fecha de vencimiento
- **Request:** `GET /b1s/v2/SBOBobService_GetDueDate`
- **Parameters:** `CardCode` (Edm.String), `RefDate` (Edm.String)
- **Returns:** Edm.String

## SBOBobService_GetIndexRate

- **Descripción (ES):** Obtener tasa del índice
- **Request:** `GET /b1s/v2/SBOBobService_GetIndexRate`
- **Parameters:** `Index` (Edm.String), `Date` (Edm.String)
- **Returns:** Edm.Double

## SBOBobService_GetLocalCurrency

- **Descripción (ES):** Obtener moneda local
- **Request:** `GET /b1s/v2/SBOBobService_GetLocalCurrency`
- **Parameters:** none
- **Returns:** Edm.String

## SBOBobService_GetSystemCurrency

- **Descripción (ES):** Obtener moneda del sistema
- **Request:** `GET /b1s/v2/SBOBobService_GetSystemCurrency`
- **Parameters:** none
- **Returns:** Edm.String

## SBOBobService_GetSystemPermission

- **Descripción (ES):** Obtener permiso del sistema
- **Request:** `GET /b1s/v2/SBOBobService_GetSystemPermission`
- **Parameters:** `UserCode` (Edm.String), `PermissionID` (Edm.String)
- **Returns:** Edm.Int32

## SBOBobService_SetCurrencyRate

- **Descripción (ES):** Establecer tipo de cambio
- **Request:** `POST /b1s/v2/SBOBobService_SetCurrencyRate`
- **Parameters:** `RateDate` (Edm.String), `Currency` (Edm.String), `Rate` (Edm.String)
- **Returns:** nothing (`204 No Content`)

```json
{
  "RateDate": "string",
  "Currency": "string",
  "Rate": "string"
}
```

## SBOBobService_SetSystemPermission

- **Descripción (ES):** Establecer permiso del sistema
- **Request:** `POST /b1s/v2/SBOBobService_SetSystemPermission`
- **Parameters:** `UserCode` (Edm.String), `PermissionID` (Edm.String), `Permission` (Edm.Int32)
- **Returns:** nothing (`204 No Content`)

```json
{
  "UserCode": "string",
  "PermissionID": "string",
  "Permission": 0
}
```

