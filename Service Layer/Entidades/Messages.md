# Messages — Mensajes

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `Messages`
- **Descripción (ES):** Mensajes
- **Entity type:** `Message`
- **Key:** `Code` (Edm.Int32)
- **DB tables (main / lines):** —
- **ETag / optimistic concurrency:** No

- **Properties:** 8 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/Messages?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/Messages/$count` | Contar |
| Get by key | `GET /b1s/v2/Messages(1)` | Obtener por clave |
| Create | `POST /b1s/v2/Messages` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/Messages(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/Messages(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/Messages(1)` (only if the B1 object allows removal) | Borrar |

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.Int32 | No | Code | Código |
| 2 | `User` | Edm.Int32 | Yes | User | Usuario |
| 3 | `Priority` | [BoMsgPriorities](../Enums/BoMsgPriorities.md) | Yes | Priority | Prioridad |
| 4 | `Subject` | Edm.String | Yes | Subject | Asunto |
| 5 | `Text` | Edm.String | Yes | Text | Texto |
| 6 | `Attachment` | Edm.Int32 | Yes | Attachment | Anexo |
| 7 | `MessageDataColumns` | Collection([MessageDataColumn](../Tipos-Complejos/MessageDataColumn.md)) | Yes | Message Data Columns | Columnas de datos del mensaje |
| 8 | `RecipientCollection` | Collection([Recipient](../Tipos-Complejos/Recipient.md)) | Yes | Recipient Collection | Colección de destinatarios |
