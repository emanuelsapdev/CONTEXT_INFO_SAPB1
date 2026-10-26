# ExternalCall — Llamada externa

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ExternalCall`
- **Descripción (ES):** Llamada externa
- **Description (EN):** External Call

- **Properties:** 10

## Properties (10)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ID` | Edm.Int32 | Yes | ID | ID |
| 2 | `Category` | Edm.Int32 | Yes | Category | Categoría |
| 3 | `Status` | [ExternalCallStatusEnum](../Enums/ExternalCallStatusEnum.md) | Yes | Status | Estado |
| 4 | `CreationDate` | Edm.DateTimeOffset | Yes | Creation Date | Fecha de creación |
| 5 | `CreationTime` | Edm.Int32 | Yes | Creation Time | Hora de creación |
| 6 | `LastUpdateDate` | Edm.DateTimeOffset | Yes | Last Update Date | Fecha de la última actualización |
| 7 | `LastUpdateTime` | Edm.Int32 | Yes | Last Update Time | Hora de la última actualización |
| 8 | `LastUpdateUserCode` | Edm.String | Yes | Last Update User Code | Código del último usuario que actualizó |
| 9 | `CallArguments` | Collection([CallArgument](../Tipos-Complejos/CallArgument.md)) | Yes | Call Arguments | Argumentos de la llamada |
| 10 | `CallMessages` | Collection([CallMessage](../Tipos-Complejos/CallMessage.md)) | Yes | Call Messages | Mensajes de la llamada |

## Used by (service operations)

- [`ExternalCallsService_GetCall`](../Servicios/ExternalCallsService.md#externalcallsservice_getcall)
- [`ExternalCallsService_SendCall`](../Servicios/ExternalCallsService.md#externalcallsservice_sendcall)
- [`ExternalCallsService_UpdateCall`](../Servicios/ExternalCallsService.md#externalcallsservice_updatecall)
