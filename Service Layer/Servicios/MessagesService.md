# MessagesService — Servicio de mensajes

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `MessagesService`
- **Descripción (ES):** Servicio de mensajes
- **Operations:** 3

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`MessagesService_GetInbox`](#messagesservice_getinbox) | function | Collection([MessageHeader](../Tipos-Complejos/MessageHeader.md)) | Get Inbox | Obtener bandeja de entrada |
| [`MessagesService_GetOutbox`](#messagesservice_getoutbox) | function | Collection([MessageHeader](../Tipos-Complejos/MessageHeader.md)) | Get Outbox | Obtener bandeja de salida |
| [`MessagesService_GetSentMessages`](#messagesservice_getsentmessages) | action | Collection([MessageHeader](../Tipos-Complejos/MessageHeader.md)) | Get Sent Messages | Obtener mensajes enviados |

## MessagesService_GetInbox

- **Descripción (ES):** Obtener bandeja de entrada
- **Request:** `GET /b1s/v2/MessagesService_GetInbox`
- **Parameters:** none
- **Returns:** Collection([MessageHeader](../Tipos-Complejos/MessageHeader.md))

## MessagesService_GetOutbox

- **Descripción (ES):** Obtener bandeja de salida
- **Request:** `GET /b1s/v2/MessagesService_GetOutbox`
- **Parameters:** none
- **Returns:** Collection([MessageHeader](../Tipos-Complejos/MessageHeader.md))

## MessagesService_GetSentMessages

- **Descripción (ES):** Obtener mensajes enviados
- **Request:** `POST /b1s/v2/MessagesService_GetSentMessages`
- **Parameters:** none
- **Returns:** Collection([MessageHeader](../Tipos-Complejos/MessageHeader.md))

