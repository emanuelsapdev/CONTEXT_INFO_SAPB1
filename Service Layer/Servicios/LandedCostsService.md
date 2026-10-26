# LandedCostsService — Servicio de costos de importación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `LandedCostsService`
- **Descripción (ES):** Servicio de costos de importación
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`LandedCostsService_GetLandedCostList`](#landedcostsservice_getlandedcostlist) | action | Collection([LandedCostParams](../Tipos-Complejos/LandedCostParams.md)) | Get Landed Cost List | Obtener lista de costos de importación |

## LandedCostsService_GetLandedCostList

- **Descripción (ES):** Obtener lista de costos de importación
- **Request:** `POST /b1s/v2/LandedCostsService_GetLandedCostList`
- **Parameters:** none
- **Returns:** Collection([LandedCostParams](../Tipos-Complejos/LandedCostParams.md))

