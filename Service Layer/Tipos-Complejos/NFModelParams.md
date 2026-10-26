# NFModelParams — Parámetros de modelos de Nota Fiscal

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `NFModelParams`
- **Descripción (ES):** Parámetros de modelos de Nota Fiscal
- **Description (EN):** NF Model Parameters

- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` | Edm.String | Yes | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `NFMName` | Edm.String | Yes | NFM Name | Nombre del modelo de NF |
| 3 | `NFMDescription` | Edm.String | Yes | NFM Description | Descripción del modelo de NF |
| 4 | `NFMCode` | Edm.String | Yes | NFM Code | Código del modelo de NF |

## Used by (service operations)

- [`NFModelsService_GetList`](../Servicios/NFModelsService.md#nfmodelsservice_getlist)
