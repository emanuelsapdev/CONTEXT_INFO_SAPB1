# MessageHeader — Cabecera de mensaje

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `MessageHeader`
- **Descripción (ES):** Cabecera de mensaje
- **Description (EN):** Message Header

- **Properties:** 7

## Properties (7)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` | Edm.Int32 | Yes | Code | Código |
| 2 | `Received` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Received | Recibido |
| 3 | `Read` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Read | Leído |
| 4 | `ReceivedDate` | Edm.DateTimeOffset | Yes | Received Date | Fecha de recepción |
| 5 | `ReceivedTime` | Edm.TimeOfDay | Yes | Received Time | Hora de recepción |
| 6 | `SentDate` | Edm.DateTimeOffset | Yes | Sent Date | Fecha de envío |
| 7 | `SentTime` | Edm.TimeOfDay | Yes | Sent Time | Hora de envío |

## Used by (service operations)

- [`MessagesService_GetInbox`](../Servicios/MessagesService.md#messagesservice_getinbox)
- [`MessagesService_GetOutbox`](../Servicios/MessagesService.md#messagesservice_getoutbox)
- [`MessagesService_GetSentMessages`](../Servicios/MessagesService.md#messagesservice_getsentmessages)
