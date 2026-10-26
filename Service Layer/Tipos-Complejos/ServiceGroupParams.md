# ServiceGroupParams — Parámetros de grupos de servicios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ServiceGroupParams`
- **Descripción (ES):** Parámetros de grupos de servicios
- **Description (EN):** Service Group Parameters

- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` | Edm.Int32 | Yes | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `ServiceGroupCode` | Edm.String | Yes | Service Group Code | Código de grupo de servicios |

## Used by (service operations)

- [`ServiceGroupsService_GetServiceGroupList`](../Servicios/ServiceGroupsService.md#servicegroupsservice_getservicegrouplist)
