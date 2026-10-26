# Activities — Actividades

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `Activities`
- **Descripción (ES):** Actividades
- **Entity type:** `Activity` (open type: accepts dynamic/UDF properties)
- **Key:** `ActivityCode` (Edm.Int32)
- **DB tables (main / lines):** [OCLG](../../Tablas%20SAP%20B1/OCLG.md)
- **ETag / optimistic concurrency:** Yes (`DataVersion`) — send `If-Match` on PATCH/DELETE/actions

- **Properties:** 76 · **Navigation properties:** 10 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/Activities?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/Activities/$count` | Contar |
| Get by key | `GET /b1s/v2/Activities(1)` | Obtener por clave |
| Create | `POST /b1s/v2/Activities` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/Activities(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/Activities(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/Activities(1)` (only if the B1 object allows removal) | Borrar |

## Properties (76)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ActivityCode` 🔑 | Edm.Int32 | No | Activity Code | Código de actividad |
| 2 | `CardCode` | Edm.String | Yes | Card Code | Código del socio de negocios |
| 3 | `Notes` | Edm.String | Yes | Notes | Notas |
| 4 | `ActivityDate` | Edm.DateTimeOffset | Yes | Activity Date | Fecha de la actividad |
| 5 | `ActivityTime` | Edm.TimeOfDay | Yes | Activity Time | Hora de la actividad |
| 6 | `StartDate` | Edm.DateTimeOffset | Yes | Start Date | Fecha de inicio |
| 7 | `Closed` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Closed | Cerrado |
| 8 | `CloseDate` | Edm.DateTimeOffset | Yes | Close Date | Fecha de cierre |
| 9 | `Phone` | Edm.String | Yes | Phone | Teléfono |
| 10 | `Fax` | Edm.String | Yes | Fax | Fax |
| 11 | `Subject` | Edm.Int32 | Yes | Subject | Asunto |
| 12 | `DocType` | Edm.String | Yes | Document Type | Tipo de documento (artículos/servicios) |
| 13 | `DocNum` | Edm.String | Yes | Document Number | Número de documento |
| 14 | `DocEntry` | Edm.String | Yes | Document Entry | DocEntry (clave interna del documento) |
| 15 | `Priority` | [BoMsgPriorities](../Enums/BoMsgPriorities.md) | Yes | Priority | Prioridad |
| 16 | `Details` | Edm.String | Yes | Details | Detalles |
| 17 | `ActivityProperty` | [BoActivities](../Enums/BoActivities.md) | Yes | Activity Property | Propiedad de la actividad |
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
| 31 | `PersonalFlag` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Personal Flag | Indicador personal |
| 32 | `Street` | Edm.String | Yes | Street | Calle |
| 33 | `ParentObjectId` | Edm.Int32 | Yes | Parent Object ID | ID del objeto padre |
| 34 | `ParentObjectType` | Edm.String | Yes | Parent Object Type | Tipo de objeto padre |
| 35 | `Room` | Edm.String | Yes | Room | Sala/oficina |
| 36 | `InactiveFlag` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Inactive Flag | Indicador de inactivo |
| 37 | `State` | Edm.String | Yes | State | Estado/provincia |
| 38 | `PreviousActivity` | Edm.Int32 | Yes | Previous Activity | Actividad anterior |
| 39 | `Country` | Edm.String | Yes | Country | País |
| 40 | `Status` | Edm.Int32 | Yes | Status | Estado |
| 41 | `TentativeFlag` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Tentative Flag | Indicador de provisorio |
| 42 | `EndDueDate` | Edm.DateTimeOffset | Yes | End Due Date | Fecha de vencimiento final |
| 43 | `DocTypeEx` | Edm.String | Yes | Document Type Ex | Tipo de documento (ampliado) |
| 44 | `AttachmentEntry` | Edm.Int32 | Yes | Attachment Entry | Entrada de anexo (ID) |
| 45 | `RecurrencePattern` | [RecurrencePatternEnum](../Enums/RecurrencePatternEnum.md) | Yes | Recurrence Pattern | Patrón de recurrencia |
| 46 | `EndType` | [EndTypeEnum](../Enums/EndTypeEnum.md) | Yes | End Type | Tipo de fin |
| 47 | `SeriesStartDate` | Edm.DateTimeOffset | Yes | Series Start Date | Fecha de inicio de la serie |
| 48 | `SeriesEndDate` | Edm.DateTimeOffset | Yes | Series End Date | Fecha de fin de la serie |
| 49 | `MaxOccurrence` | Edm.Int32 | Yes | Max Occurrence | Ocurrencias máximas |
| 50 | `Interval` | Edm.Int32 | Yes | Interval | Intervalo |
| 51 | `Sunday` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Sunday | Domingo |
| 52 | `Monday` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Monday | Lunes |
| 53 | `Tuesday` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Tuesday | Martes |
| 54 | `Wednesday` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Wednesday | Miércoles |
| 55 | `Thursday` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Thursday | Jueves |
| 56 | `Friday` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Friday | Viernes |
| 57 | `Saturday` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Saturday | Sábado |
| 58 | `RepeatOption` | [RepeatOptionEnum](../Enums/RepeatOptionEnum.md) | Yes | Repeat Option | Opción de repetición |
| 59 | `BelongedSeriesNum` | Edm.Int32 | Yes | Belonged Series Number | Número de serie al que pertenece |
| 60 | `IsRemoved` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Removed | Está eliminado |
| 61 | `AddressName` | Edm.String | Yes | Address Name | Nombre de dirección |
| 62 | `AddressType` | [BoAddressType](../Enums/BoAddressType.md) | Yes | Address Type | Tipo de dirección |
| 63 | `HandledByEmployee` | Edm.Int32 | Yes | Handled By Employee | Gestionado por empleado |
| 64 | `RecurrenceSequenceSpecifier` | [RecurrenceSequenceEnum](../Enums/RecurrenceSequenceEnum.md) | Yes | Recurrence Sequence Specifier | Especificador de secuencia de recurrencia |
| 65 | `RecurrenceDayInMonth` | Edm.Int32 | Yes | Recurrence Day In Month | Día del mes de recurrencia |
| 66 | `RecurrenceMonth` | Edm.Int32 | Yes | Recurrence Month | Mes de recurrencia |
| 67 | `RecurrenceDayOfWeek` | [RecurrenceDayOfWeekEnum](../Enums/RecurrenceDayOfWeekEnum.md) | Yes | Recurrence Day Of Week | Día de la semana de recurrencia |
| 68 | `SalesOpportunityId` | Edm.Int32 | Yes | Sales Opportunity ID | ID de oportunidad de venta |
| 69 | `SalesOpportunityLine` | Edm.Int32 | Yes | Sales Opportunity Line | Línea de oportunidad de venta |
| 70 | `HandledByRecipientList` | Edm.Int32 | Yes | Handled By Recipient List | Gestionado por lista de destinatarios |
| 71 | `Office365EventId` | Edm.String | Yes | Office 365 Event ID | ID de evento de Office 365 |
| 72 | `DataVersion` | Edm.Int32 | Yes | Data Version | Versión de datos (control de concurrencia) |
| 73 | `UserSignature` | Edm.Int32 | Yes | User Signature | Firma del usuario |
| 74 | `UserSignature2` | Edm.Int32 | Yes | User Signature 2 | Firma del usuario 2 (último en modificar) |
| 75 | `CheckInListParams` | Collection([CheckInParams](../Tipos-Complejos/CheckInParams.md)) | Yes | Check In List Parameters | Parámetros de lista de check-in |
| 76 | `ActivityMultipleRecipients` | Collection([ActivityMultipleRecipient](../Tipos-Complejos/ActivityMultipleRecipient.md)) | Yes | Activity Multiple Recipients | Destinatarios múltiples de la actividad |

## Navigation properties (10)

Use `GET /b1s/v2/Activities(1)/<Navigation>` or `$expand=<Navigation>`.

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
| `EmployeeInfo` | [EmployeeInfo](../Entidades/EmployeesInfo.md) | [EmployeesInfo](EmployeesInfo.md) | HandledByEmployee → EmployeeID | Empleados |
| `ActivityRecipientList` | [ActivityRecipientList](../Entidades/ActivityRecipientLists.md) | [ActivityRecipientLists](ActivityRecipientLists.md) | HandledByRecipientList → Code | Listas de destinatarios de actividades |

## Service operations that use this type

- [`ActivitiesService_GetListByAttendUser`](../Servicios/ActivitiesService.md#activitiesservice_getlistbyattenduser)
- [`ActivitiesService_GetSingleInstanceFromSeries`](../Servicios/ActivitiesService.md#activitiesservice_getsingleinstancefromseries)
- [`ActivitiesService_InitData`](../Servicios/ActivitiesService.md#activitiesservice_initdata)
- [`ActivitiesService_UpdateSingleInstanceInSeries`](../Servicios/ActivitiesService.md#activitiesservice_updatesingleinstanceinseries)
