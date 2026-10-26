# ResourceCapacitiesService — Servicio de capacidades de recursos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `ResourceCapacitiesService`
- **Descripción (ES):** Servicio de capacidades de recursos
- **Operations:** 2

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`ResourceCapacitiesService_GetList`](#resourcecapacitiesservice_getlist) | action | Collection([ResourceCapacityParams](../Tipos-Complejos/ResourceCapacityParams.md)) | Get List | Obtener lista |
| [`ResourceCapacitiesService_GetListWithFilter`](#resourcecapacitiesservice_getlistwithfilter) | action | Collection([ResourceCapacityParams](../Tipos-Complejos/ResourceCapacityParams.md)) | Get List With Filter | Obtener lista con filtro |

## ResourceCapacitiesService_GetList

- **Descripción (ES):** Obtener lista
- **Request:** `POST /b1s/v2/ResourceCapacitiesService_GetList`
- **Parameters:** none
- **Returns:** Collection([ResourceCapacityParams](../Tipos-Complejos/ResourceCapacityParams.md))

## ResourceCapacitiesService_GetListWithFilter

- **Descripción (ES):** Obtener lista con filtro
- **Request:** `POST /b1s/v2/ResourceCapacitiesService_GetListWithFilter`
- **Parameters:** `ResourceCapacityWithFilterParams` ([ResourceCapacityWithFilterParams](../Tipos-Complejos/ResourceCapacityWithFilterParams.md))
- **Returns:** Collection([ResourceCapacityParams](../Tipos-Complejos/ResourceCapacityParams.md))

```json
{
  "ResourceCapacityWithFilterParams": {
    "Code": "string",
    "Warehouse": "string",
    "Date": "2026-01-31",
    ...
  }
}
```

