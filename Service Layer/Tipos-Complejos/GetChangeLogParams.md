# GetChangeLogParams — Parámetros para obtener registro de modificaciones

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `GetChangeLogParams`
- **Descripción (ES):** Parámetros para obtener registro de modificaciones
- **Description (EN):** Get Change Log Parameters

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `PrimaryKey` | Edm.String | Yes | Primary Key | Clave primaria |
| 2 | `UDOObjectCode` | Edm.String | Yes | UDO Object Code | Código de objeto UDO |
| 3 | `Object` | [BoChangeLogEnum](../Enums/BoChangeLogEnum.md) | Yes | Object | Objeto |

## Used by (service operations)

- [`ChangeLogsService_GetChangeLog`](../Servicios/ChangeLogsService.md#changelogsservice_getchangelog)
