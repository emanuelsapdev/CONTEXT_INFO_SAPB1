# CallMessage — Mensajes de la llamada

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `CallMessage`
- **Descripción (ES):** Mensajes de la llamada
- **Description (EN):** Call Message

- **Properties:** 8

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ID` | Edm.Int32 | Yes | ID | ID |
| 2 | `Type` | [CallMessageTypeEnum](../Enums/CallMessageTypeEnum.md) | Yes | Type | Tipo |
| 3 | `ErrorCode` | Edm.String | Yes | Error Code | Código de error |
| 4 | `MessageBody` | Edm.String | Yes | Message Body | Cuerpo del mensaje |
| 5 | `Status` | [CallMessageStatusEnum](../Enums/CallMessageStatusEnum.md) | Yes | Status | Estado |
| 6 | `CreationDate` | Edm.DateTimeOffset | Yes | Creation Date | Fecha de creación |
| 7 | `CreationTime` | Edm.Int32 | Yes | Creation Time | Hora de creación |
| 8 | `CallMessageArguments` | Collection([CallMessageArgument](../Tipos-Complejos/CallMessageArgument.md)) | Yes | Call Message Arguments | Argumentos de mensajes de la llamada |

## Used by (properties)

- [ExternalCall](ExternalCall.md).`CallMessages`
