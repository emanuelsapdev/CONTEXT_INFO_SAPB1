# OccurenceCodeParams — Parámetros de códigos de ocurrencia

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `OccurenceCodeParams`
- **Descripción (ES):** Parámetros de códigos de ocurrencia
- **Description (EN):** Occurence Code Parameters

- **Properties:** 6

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` | Edm.Int32 | Yes | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `Code` | Edm.String | Yes | Code | Código |
| 3 | `Description` | Edm.String | Yes | Description | Descripción |
| 4 | `Note` | Edm.String | Yes | Note | Nota |
| 5 | `RequestedBoeStatus` | [BoBoeStatus](../Enums/BoBoeStatus.md) | Yes | Requested Boe Status | Estado solicitado de la letra de cambio |
| 6 | `IsMovement` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Movement | Es movimiento |

## Used by (service operations)

- [`OccurrenceCodesService_GetList`](../Servicios/OccurrenceCodesService.md#occurrencecodesservice_getlist)
