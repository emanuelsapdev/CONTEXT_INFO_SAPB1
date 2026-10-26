# ChangeLogParams — Parámetros del registro de modificaciones

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ChangeLogParams`
- **Descripción (ES):** Parámetros del registro de modificaciones
- **Description (EN):** Change Log Parameters

- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LogInstance` | Edm.Int32 | Yes | Log Instance | Instancia de registro (historial) |
| 2 | `UpdatedDate` | Edm.DateTimeOffset | Yes | Updated Date | Fecha de actualización |
| 3 | `UserName` | Edm.String | Yes | User Name | Nombre de usuario |
| 4 | `ObjectCode` | Edm.String | Yes | Object Code | Código de objeto |

## Used by (service operations)

- [`ChangeLogsService_GetChangeLog`](../Servicios/ChangeLogsService.md#changelogsservice_getchangelog)
