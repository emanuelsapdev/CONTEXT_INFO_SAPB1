# UsersService — Servicio de usuarios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `UsersService`
- **Descripción (ES):** Servicio de usuarios
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`UsersService_GetCurrentUser`](#usersservice_getcurrentuser) | action | [User](../Entidades/Users.md) | Get Current User | Obtener usuario actual |

## UsersService_GetCurrentUser

- **Descripción (ES):** Obtener usuario actual
- **Request:** `POST /b1s/v2/UsersService_GetCurrentUser`
- **Parameters:** none
- **Returns:** [User](../Entidades/Users.md)

