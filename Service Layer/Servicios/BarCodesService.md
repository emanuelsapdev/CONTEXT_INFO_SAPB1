# BarCodesService — Servicio de códigos de barras

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `BarCodesService`
- **Descripción (ES):** Servicio de códigos de barras
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`BarCodesService_GetList`](#barcodesservice_getlist) | action | Collection([BarCodeParams](../Tipos-Complejos/BarCodeParams.md)) | Get List | Obtener lista |

## BarCodesService_GetList

- **Descripción (ES):** Obtener lista
- **Request:** `POST /b1s/v2/BarCodesService_GetList`
- **Parameters:** none
- **Returns:** Collection([BarCodeParams](../Tipos-Complejos/BarCodeParams.md))

