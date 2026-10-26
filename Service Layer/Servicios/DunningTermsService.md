# DunningTermsService — Servicio de condiciones de reclamación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `DunningTermsService`
- **Descripción (ES):** Servicio de condiciones de reclamación
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`DunningTermsService_GetDunningTermList`](#dunningtermsservice_getdunningtermlist) | action | Collection([DunningTermParams](../Tipos-Complejos/DunningTermParams.md)) | Get Dunning Term List | Obtener lista de condiciones de reclamación |

## DunningTermsService_GetDunningTermList

- **Descripción (ES):** Obtener lista de condiciones de reclamación
- **Request:** `POST /b1s/v2/DunningTermsService_GetDunningTermList`
- **Parameters:** none
- **Returns:** Collection([DunningTermParams](../Tipos-Complejos/DunningTermParams.md))

