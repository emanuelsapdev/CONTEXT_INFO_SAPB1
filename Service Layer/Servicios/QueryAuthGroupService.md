# QueryAuthGroupService — Servicio de grupos de autorización de consultas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `QueryAuthGroupService`
- **Descripción (ES):** Servicio de grupos de autorización de consultas
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`QueryAuthGroupService_GetQueryAuthGroupList`](#queryauthgroupservice_getqueryauthgrouplist) | action | Collection([QueryAuthGroup](../Entidades/QueryAuthGroups.md)) | Get Query Auth Group List | Obtener lista de grupos de autorización de consultas |

## QueryAuthGroupService_GetQueryAuthGroupList

- **Descripción (ES):** Obtener lista de grupos de autorización de consultas
- **Request:** `POST /b1s/v2/QueryAuthGroupService_GetQueryAuthGroupList`
- **Parameters:** none
- **Returns:** Collection([QueryAuthGroup](../Entidades/QueryAuthGroups.md))

