# UserMenuService — Servicio de menú de usuario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `UserMenuService`
- **Descripción (ES):** Servicio de menú de usuario
- **Operations:** 4

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`UserMenuService_GetCurrentUserMenu`](#usermenuservice_getcurrentusermenu) | function | Collection([UserMenuItem](../Tipos-Complejos/UserMenuItem.md)) | Get Current User Menu | Obtener menú del usuario actual |
| [`UserMenuService_GetUserMenu`](#usermenuservice_getusermenu) | action | Collection([UserMenuItem](../Tipos-Complejos/UserMenuItem.md)) | Get User Menu | Obtener menú de usuario |
| [`UserMenuService_UpdateCurrentUserMenu`](#usermenuservice_updatecurrentusermenu) | action | — | Update Current User Menu | Actualizar menú del usuario actual |
| [`UserMenuService_UpdateUserMenu`](#usermenuservice_updateusermenu) | action | — | Update User Menu | Actualizar menú de usuario |

## UserMenuService_GetCurrentUserMenu

- **Descripción (ES):** Obtener menú del usuario actual
- **Request:** `GET /b1s/v2/UserMenuService_GetCurrentUserMenu`
- **Parameters:** none
- **Returns:** Collection([UserMenuItem](../Tipos-Complejos/UserMenuItem.md))

## UserMenuService_GetUserMenu

- **Descripción (ES):** Obtener menú de usuario
- **Request:** `POST /b1s/v2/UserMenuService_GetUserMenu`
- **Parameters:** `UserMenuParams` ([UserMenuParams](../Tipos-Complejos/UserMenuParams.md))
- **Returns:** Collection([UserMenuItem](../Tipos-Complejos/UserMenuItem.md))

```json
{
  "UserMenuParams": {
    "UserID": 0
  }
}
```

## UserMenuService_UpdateCurrentUserMenu

- **Descripción (ES):** Actualizar menú del usuario actual
- **Request:** `POST /b1s/v2/UserMenuService_UpdateCurrentUserMenu`
- **Parameters:** `UserMenuItems` (Collection([UserMenuItem](../Tipos-Complejos/UserMenuItem.md)))
- **Returns:** nothing (`204 No Content`)

```json
{
  "UserMenuItems": [ {
    "Name": "string",
    "Position": 0,
    "LinkedObjType": "string",
    "LinkedObjKey": "string",
    ...
  } ]
}
```

## UserMenuService_UpdateUserMenu

- **Descripción (ES):** Actualizar menú de usuario
- **Request:** `POST /b1s/v2/UserMenuService_UpdateUserMenu`
- **Parameters:** `UserMenuParams` ([UserMenuParams](../Tipos-Complejos/UserMenuParams.md)), `UserMenuItems` (Collection([UserMenuItem](../Tipos-Complejos/UserMenuItem.md)))
- **Returns:** nothing (`204 No Content`)

```json
{
  "UserMenuParams": {
    "UserID": 0
  },
  "UserMenuItems": [ {
    "Name": "string",
    "Position": 0,
    "LinkedObjType": "string",
    "LinkedObjKey": "string",
    ...
  } ]
}
```

