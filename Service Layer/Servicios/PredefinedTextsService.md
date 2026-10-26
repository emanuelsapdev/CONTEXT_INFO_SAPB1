# PredefinedTextsService — Servicio de textos predefinidos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `PredefinedTextsService`
- **Descripción (ES):** Servicio de textos predefinidos
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`PredefinedTextsService_GetPredefinedTextList`](#predefinedtextsservice_getpredefinedtextlist) | action | Collection([PredefinedTextParams](../Tipos-Complejos/PredefinedTextParams.md)) | Get Predefined Text List | Obtener lista de textos predefinidos |

## PredefinedTextsService_GetPredefinedTextList

- **Descripción (ES):** Obtener lista de textos predefinidos
- **Request:** `POST /b1s/v2/PredefinedTextsService_GetPredefinedTextList`
- **Parameters:** none
- **Returns:** Collection([PredefinedTextParams](../Tipos-Complejos/PredefinedTextParams.md))

