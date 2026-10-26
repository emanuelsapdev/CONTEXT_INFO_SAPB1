# MaterialRevaluationFIFOParams — Parámetros de revalorización FIFO

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `MaterialRevaluationFIFOParams`
- **Descripción (ES):** Parámetros de revalorización FIFO
- **Description (EN):** Material Revaluation FIFO Parameters

- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |
| 2 | `LocationType` | Edm.String | Yes | Location Type | Tipo de ubicación |
| 3 | `LocationCode` | Edm.String | Yes | Location Code | Código de ubicación |
| 4 | `ShowIssuedLayers` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Show Issued Layers | Mostrar capas emitidas |

## Used by (service operations)

- [`MaterialRevaluationFIFOService_GetMaterialRevaluationFIFO`](../Servicios/MaterialRevaluationFIFOService.md#materialrevaluationfifoservice_getmaterialrevaluationfifo)
