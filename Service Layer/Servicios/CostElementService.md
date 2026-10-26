# CostElementService — Servicio de elementos de costo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `CostElementService`
- **Descripción (ES):** Servicio de elementos de costo
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`CostElementService_GetCostElementList`](#costelementservice_getcostelementlist) | action | Collection([CostElementParams](../Tipos-Complejos/CostElementParams.md)) | Get Cost Element List | Obtener lista de elementos de costo |

## CostElementService_GetCostElementList

- **Descripción (ES):** Obtener lista de elementos de costo
- **Request:** `POST /b1s/v2/CostElementService_GetCostElementList`
- **Parameters:** none
- **Returns:** Collection([CostElementParams](../Tipos-Complejos/CostElementParams.md))

