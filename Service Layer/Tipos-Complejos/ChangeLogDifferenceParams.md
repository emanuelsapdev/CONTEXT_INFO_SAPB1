# ChangeLogDifferenceParams — Parámetros de diferencias del registro de modificaciones

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ChangeLogDifferenceParams`
- **Descripción (ES):** Parámetros de diferencias del registro de modificaciones
- **Description (EN):** Change Log Difference Parameters

- **Properties:** 7

## Properties (7)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Date` | Edm.DateTimeOffset | Yes | Date | Fecha |
| 2 | `ChangedField` | Edm.String | Yes | Changed Field | Campo modificado |
| 3 | `OldValue` | Edm.String | Yes | Old Value | Valor anterior |
| 4 | `NewValue` | Edm.String | Yes | New Value | Nuevo valor |
| 5 | `UserName` | Edm.String | Yes | User Name | Nombre de usuario |
| 6 | `ArrayOffset` | Edm.Int32 | Yes | Array Offset | Desplazamiento en la matriz |
| 7 | `LineNumber` | Edm.String | Yes | Line Number | Número de línea |

## Used by (service operations)

- [`ChangeLogsService_GetChangeLogDifferences`](../Servicios/ChangeLogsService.md#changelogsservice_getchangelogdifferences)
