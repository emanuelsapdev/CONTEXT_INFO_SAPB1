# CUPCodeService — Servicio de códigos CUP

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `CUPCodeService`
- **Descripción (ES):** Servicio de códigos CUP
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`CUPCodeService_GetList`](#cupcodeservice_getlist) | action | Collection([CUPCodeParams](../Tipos-Complejos/CUPCodeParams.md)) | Get List | Obtener lista |

## CUPCodeService_GetList

- **Descripción (ES):** Obtener lista
- **Request:** `POST /b1s/v2/CUPCodeService_GetList`
- **Parameters:** none
- **Returns:** Collection([CUPCodeParams](../Tipos-Complejos/CUPCodeParams.md))

