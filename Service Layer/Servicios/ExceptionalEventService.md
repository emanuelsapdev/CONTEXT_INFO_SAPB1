# ExceptionalEventService — Servicio de eventos excepcionales

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `ExceptionalEventService`
- **Descripción (ES):** Servicio de eventos excepcionales
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`ExceptionalEventService_GetExceptionalEventList`](#exceptionaleventservice_getexceptionaleventlist) | action | Collection([ExceptionalEventParams](../Tipos-Complejos/ExceptionalEventParams.md)) | Get Exceptional Event List | Obtener lista de eventos excepcionales |

## ExceptionalEventService_GetExceptionalEventList

- **Descripción (ES):** Obtener lista de eventos excepcionales
- **Request:** `POST /b1s/v2/ExceptionalEventService_GetExceptionalEventList`
- **Parameters:** none
- **Returns:** Collection([ExceptionalEventParams](../Tipos-Complejos/ExceptionalEventParams.md))

