# ValueMappingCommunication — Comunicación de mapeo de valores

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ValueMappingCommunication`
- **Descripción (ES):** Comunicación de mapeo de valores
- **Entity type:** `ValueMappingCommunicationData`
- **Key:** `AbsEntry` (Edm.Int32)
- **DB tables (main / lines):** [OVMC](../../Tablas%20SAP%20B1/OVMC.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 10 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ValueMappingCommunication?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ValueMappingCommunication/$count` | Contar |
| Get by key | `GET /b1s/v2/ValueMappingCommunication(1)` | Obtener por clave |
| Create | `POST /b1s/v2/ValueMappingCommunication` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ValueMappingCommunication(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ValueMappingCommunication(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/ValueMappingCommunication(1)` (only if the B1 object allows removal) | Borrar |

## Properties (10)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` 🔑 | Edm.Int32 | No | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `ThirdPartySystemId` | Edm.Int32 | Yes | Third Party System ID | ID del sistema de terceros |
| 3 | `ObjectId` | Edm.Int32 | Yes | Object ID | ID de objeto |
| 4 | `CommunicationType` | [VMCommunicationTypeEnum](../Enums/VMCommunicationTypeEnum.md) | Yes | Communication Type | Tipo de comunicación |
| 5 | `StartDate` | Edm.DateTimeOffset | Yes | Start Date | Fecha de inicio |
| 6 | `StartTime` | Edm.Int32 | Yes | Start Time | Hora de inicio |
| 7 | `EndDate` | Edm.DateTimeOffset | Yes | End Date | Fecha de fin |
| 8 | `EndTime` | Edm.Int32 | Yes | End Time | Hora de fin |
| 9 | `Message` | Edm.String | Yes | Message | Mensaje |
| 10 | `Status` | [VMCommunicationStatusEnum](../Enums/VMCommunicationStatusEnum.md) | Yes | Status | Estado |
