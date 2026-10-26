# Contacts — Contactos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `Contacts`
- **Descripción (ES):** Contactos
- **Entity type:** `Contact` (open type: accepts dynamic/UDF properties)
- **Key:** `ContactCode` (Edm.Int32)
- **DB tables (main / lines):** [OCLG](../../Tablas%20SAP%20B1/OCLG.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 47 · **Navigation properties:** 8 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/Contacts?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/Contacts/$count` | Contar |
| Get by key | `GET /b1s/v2/Contacts(1)` | Obtener por clave |
| Create | `POST /b1s/v2/Contacts` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/Contacts(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/Contacts(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/Contacts(1)` (only if the B1 object allows removal) | Borrar |

## Properties (47)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `CardCode` | Edm.String | Yes | Card Code | Código del socio de negocios |
| 2 | `Notes` | Edm.String | Yes | Notes | Notas |
| 3 | `ContactDate` | Edm.DateTimeOffset | Yes | Contact Date | Fecha de contacto |
| 4 | `ContactTime` | Edm.TimeOfDay | Yes | Contact Time | Hora de contacto |
| 5 | `Recontact` | Edm.DateTimeOffset | Yes | Recontact | Volver a contactar |
| 6 | `Closed` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Closed | Cerrado |
| 7 | `CloseDate` | Edm.DateTimeOffset | Yes | Close Date | Fecha de cierre |
| 8 | `Phone` | Edm.String | Yes | Phone | Teléfono |
| 9 | `Fax` | Edm.String | Yes | Fax | Fax |
| 10 | `Subject` | Edm.Int32 | Yes | Subject | Asunto |
| 11 | `DocType` | Edm.String | Yes | Document Type | Tipo de documento (artículos/servicios) |
| 12 | `DocNum` | Edm.String | Yes | Document Number | Número de documento |
| 13 | `DocEntry` | Edm.String | Yes | Document Entry | DocEntry (clave interna del documento) |
| 14 | `ContactCode` 🔑 | Edm.Int32 | No | Contact Code | Código de contacto |
| 15 | `Priority` | [BoMsgPriorities](../Enums/BoMsgPriorities.md) | Yes | Priority | Prioridad |
| 16 | `Details` | Edm.String | Yes | Details | Detalles |
| 17 | `Activity` | [BoActivities](../Enums/BoActivities.md) | Yes | Activity | Actividad |
| 18 | `ActivityType` | Edm.Int32 | Yes | Activity Type | Tipo de actividad |
| 19 | `Location` | Edm.Int32 | Yes | Location | Ubicación |
| 20 | `StartTime` | Edm.TimeOfDay | Yes | Start Time | Hora de inicio |
| 21 | `EndTime` | Edm.TimeOfDay | Yes | End Time | Hora de fin |
| 22 | `Duration` | Edm.Double | Yes | Duration | Duración |
| 23 | `DurationType` | [BoDurations](../Enums/BoDurations.md) | Yes | Duration Type | Tipo de duración |
| 24 | `SalesEmployee` | Edm.Int32 | Yes | Sales Employee | Empleado de ventas |
| 25 | `ContactPersonCode` | Edm.Int32 | Yes | Contact Person Code | Código de persona de contacto |
| 26 | `HandledBy` | Edm.Int32 | Yes | Handled By | Gestionado por |
| 27 | `Reminder` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Reminder | Recordatorio |
| 28 | `ReminderPeriod` | Edm.Double | Yes | Reminder Period | Período del recordatorio |
| 29 | `ReminderType` | [BoDurations](../Enums/BoDurations.md) | Yes | Reminder Type | Tipo de recordatorio |
| 30 | `City` | Edm.String | Yes | City | Ciudad |
| 31 | `Personalflag` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Personalflag | Indicador personal |
| 32 | `Street` | Edm.String | Yes | Street | Calle |
| 33 | `ParentobjectId` | Edm.Int32 | Yes | Parentobject ID | ID del objeto padre |
| 34 | `Parentobjecttype` | Edm.String | Yes | Parentobjecttype | Tipo de objeto padre |
| 35 | `Room` | Edm.String | Yes | Room | Sala/oficina |
| 36 | `Inactiveflag` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Inactiveflag | Indicador de inactivo |
| 37 | `State` | Edm.String | Yes | State | Estado/provincia |
| 38 | `PreviousActivity` | Edm.Int32 | Yes | Previous Activity | Actividad anterior |
| 39 | `Country` | Edm.String | Yes | Country | País |
| 40 | `Status` | Edm.Int32 | Yes | Status | Estado |
| 41 | `Tentativeflag` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Tentativeflag | Indicador de provisorio |
| 42 | `EndDuedate` | Edm.DateTimeOffset | Yes | End Duedate | Fecha de vencimiento final |
| 43 | `DocTypeEx` | Edm.String | Yes | Document Type Ex | Tipo de documento (ampliado) |
| 44 | `AttachmentEntry` | Edm.Int32 | Yes | Attachment Entry | Entrada de anexo (ID) |
| 45 | `StartDate` | Edm.DateTimeOffset | Yes | Start Date | Fecha de inicio |
| 46 | `UserSignature` | Edm.Int32 | Yes | User Signature | Firma del usuario |
| 47 | `UserSignature2` | Edm.Int32 | Yes | User Signature 2 | Firma del usuario 2 (último en modificar) |

## Navigation properties (8)

Use `GET /b1s/v2/Contacts(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `BusinessPartner` | [BusinessPartner](../Entidades/BusinessPartners.md) | [BusinessPartners](BusinessPartners.md) | CardCode → CardCode | Socio de negocios |
| `ActivitySubject` | [ActivitySubject](../Entidades/ActivitySubjects.md) | [ActivitySubjects](ActivitySubjects.md) | Subject → Code | Asuntos de actividades |
| `ActivityType2` | [ActivityType](../Entidades/ActivityTypes.md) | [ActivityTypes](ActivityTypes.md) | ActivityType → Code | Tipos de actividades |
| `ActivityLocation` | [ActivityLocation](../Entidades/ActivityLocations.md) | [ActivityLocations](ActivityLocations.md) | Location → Code | Lugares de actividades |
| `SalesPerson` | [SalesPerson](../Entidades/SalesPersons.md) | [SalesPersons](SalesPersons.md) | SalesEmployee → SalesEmployeeCode | Empleado de ventas |
| `User` | [User](../Entidades/Users.md) | [Users](Users.md) | HandledBy → InternalKey | Usuario |
| `Country2` | [Country](../Entidades/Countries.md) | [Countries](Countries.md) | Country → Code | Países/Regiones |
| `ActivityStatus` | [ActivityStatus](../Entidades/ActivityStatuses.md) | [ActivityStatuses](ActivityStatuses.md) | Status → StatusId | Estados de actividades |
