# UserGroupService — Servicio de grupos de usuarios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `UserGroupService`
- **Descripción (ES):** Servicio de grupos de usuarios
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`UserGroupService_GetUserGroupList`](#usergroupservice_getusergrouplist) | action | Collection([UserGroupParams](../Tipos-Complejos/UserGroupParams.md)) | Get User Group List | Obtener lista de grupos de usuarios |

## UserGroupService_GetUserGroupList

- **Descripción (ES):** Obtener lista de grupos de usuarios
- **Request:** `POST /b1s/v2/UserGroupService_GetUserGroupList`
- **Parameters:** none
- **Returns:** Collection([UserGroupParams](../Tipos-Complejos/UserGroupParams.md))

