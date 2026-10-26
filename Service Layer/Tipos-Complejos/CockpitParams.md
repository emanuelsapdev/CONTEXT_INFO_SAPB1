# CockpitParams — Parámetros de cockpits

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `CockpitParams`
- **Descripción (ES):** Parámetros de cockpits
- **Description (EN):** Cockpit Parameters

- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` | Edm.Int32 | Yes | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `CockpitType` | [BoCockpitTypeEnum](../Enums/BoCockpitTypeEnum.md) | Yes | Cockpit Type | Tipo de cockpit |

## Used by (service operations)

- [`CockpitsService_GetCockpitList`](../Servicios/CockpitsService.md#cockpitsservice_getcockpitlist)
- [`CockpitsService_GetTemplateCockpitList`](../Servicios/CockpitsService.md#cockpitsservice_gettemplatecockpitlist)
- [`CockpitsService_GetUserCockpitList`](../Servicios/CockpitsService.md#cockpitsservice_getusercockpitlist)
