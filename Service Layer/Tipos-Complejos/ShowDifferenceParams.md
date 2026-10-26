# ShowDifferenceParams — Parámetros para mostrar diferencias

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ShowDifferenceParams`
- **Descripción (ES):** Parámetros para mostrar diferencias
- **Description (EN):** Show Difference Parameters

- **Properties:** 5

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `PrimaryKey` | Edm.String | Yes | Primary Key | Clave primaria |
| 2 | `UDOObjectCode` | Edm.String | Yes | UDO Object Code | Código de objeto UDO |
| 3 | `Object` | [BoChangeLogEnum](../Enums/BoChangeLogEnum.md) | Yes | Object | Objeto |
| 4 | `LogInstance2` | Edm.Int32 | Yes | Log Instance 2 | Instancia de registro 2 |
| 5 | `LogInstance` | Edm.Int32 | Yes | Log Instance | Instancia de registro (historial) |

## Used by (service operations)

- [`ChangeLogsService_GetChangeLogDifferences`](../Servicios/ChangeLogsService.md#changelogsservice_getchangelogdifferences)
