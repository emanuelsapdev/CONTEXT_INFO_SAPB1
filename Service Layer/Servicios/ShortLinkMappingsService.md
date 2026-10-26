# ShortLinkMappingsService — Servicio de mapeo de vínculos cortos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `ShortLinkMappingsService`
- **Descripción (ES):** Servicio de mapeo de vínculos cortos
- **Operations:** 2

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`ShortLinkMappingsService_BatchDelete`](#shortlinkmappingsservice_batchdelete) | action | — | Batch Delete | Eliminar en lote |
| [`ShortLinkMappingsService_GetList`](#shortlinkmappingsservice_getlist) | action | Collection([ShortLinkMappingParams](../Tipos-Complejos/ShortLinkMappingParams.md)) | Get List | Obtener lista |

## ShortLinkMappingsService_BatchDelete

- **Descripción (ES):** Eliminar en lote
- **Request:** `POST /b1s/v2/ShortLinkMappingsService_BatchDelete`
- **Parameters:** none
- **Returns:** nothing (`204 No Content`)

## ShortLinkMappingsService_GetList

- **Descripción (ES):** Obtener lista
- **Request:** `POST /b1s/v2/ShortLinkMappingsService_GetList`
- **Parameters:** none
- **Returns:** Collection([ShortLinkMappingParams](../Tipos-Complejos/ShortLinkMappingParams.md))

