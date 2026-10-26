# MaterialRevaluationFIFOService — Servicio de revalorización FIFO

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `MaterialRevaluationFIFOService`
- **Descripción (ES):** Servicio de revalorización FIFO
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`MaterialRevaluationFIFOService_GetMaterialRevaluationFIFO`](#materialrevaluationfifoservice_getmaterialrevaluationfifo) | action | [MaterialRevaluationFIFO](../Tipos-Complejos/MaterialRevaluationFIFO.md) | Get Material Revaluation FIFO | Obtener revalorización FIFO |

## MaterialRevaluationFIFOService_GetMaterialRevaluationFIFO

- **Descripción (ES):** Obtener revalorización FIFO
- **Request:** `POST /b1s/v2/MaterialRevaluationFIFOService_GetMaterialRevaluationFIFO`
- **Parameters:** `MaterialRevaluationFIFOParams` ([MaterialRevaluationFIFOParams](../Tipos-Complejos/MaterialRevaluationFIFOParams.md))
- **Returns:** [MaterialRevaluationFIFO](../Tipos-Complejos/MaterialRevaluationFIFO.md)

```json
{
  "MaterialRevaluationFIFOParams": {
    "ItemCode": "string",
    "LocationType": "string",
    "LocationCode": "string",
    ...
  }
}
```

