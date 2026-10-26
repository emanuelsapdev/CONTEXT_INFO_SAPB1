# StatesService — Servicio de estados/provincias

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `StatesService`
- **Descripción (ES):** Servicio de estados/provincias
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`StatesService_GetStateList`](#statesservice_getstatelist) | action | Collection([StateParams](../Tipos-Complejos/StateParams.md)) | Get State List | Obtener lista de estados/provincias |

## StatesService_GetStateList

- **Descripción (ES):** Obtener lista de estados/provincias
- **Request:** `POST /b1s/v2/StatesService_GetStateList`
- **Parameters:** none
- **Returns:** Collection([StateParams](../Tipos-Complejos/StateParams.md))

