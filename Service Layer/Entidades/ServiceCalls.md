# ServiceCalls — Llamadas de servicio

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ServiceCalls`
- **Descripción (ES):** Llamadas de servicio
- **Entity type:** `ServiceCall` (open type: accepts dynamic/UDF properties)
- **Key:** `ServiceCallID` (Edm.Int32)
- **DB tables (main / lines):** [OSCL](../../Tablas%20SAP%20B1/OSCL.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 87 · **Navigation properties:** 15 · **Bound actions:** 1

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ServiceCalls?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ServiceCalls/$count` | Contar |
| Get by key | `GET /b1s/v2/ServiceCalls(1)` | Obtener por clave |
| Create | `POST /b1s/v2/ServiceCalls` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ServiceCalls(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ServiceCalls(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/ServiceCalls(1)` (only if the B1 object allows removal) | Borrar |
| Action `Close` | `POST /b1s/v2/ServiceCalls(1)/Close` | Cerrar |

## Properties (87)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ServiceCallID` 🔑 | Edm.Int32 | No | Service Call ID | ID de llamada de servicio |
| 2 | `Subject` | Edm.String | Yes | Subject | Asunto |
| 3 | `CustomerCode` | Edm.String | Yes | Customer Code | Código de cliente |
| 4 | `CustomerName` | Edm.String | Yes | Customer Name | Nombre del cliente |
| 5 | `ContactCode` | Edm.Int32 | Yes | Contact Code | Código de contacto |
| 6 | `ManufacturerSerialNum` | Edm.String | Yes | Manufacturer Serial Number | Número de serie del fabricante |
| 7 | `InternalSerialNum` | Edm.String | Yes | Internal Serial Number | Número de serie interno |
| 8 | `ContractID` | Edm.Int32 | Yes | Contract ID | ID de contrato |
| 9 | `ContractEndDate` | Edm.DateTimeOffset | Yes | Contract End Date | Fecha de fin del contrato |
| 10 | `ResolutionDate` | Edm.DateTimeOffset | Yes | Resolution Date | Fecha de resolución |
| 11 | `ResolutionTime` | Edm.TimeOfDay | Yes | Resolution Time | Tiempo de resolución |
| 12 | `Origin` | Edm.Int32 | Yes | Origin | Origen |
| 13 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |
| 14 | `ItemDescription` | Edm.String | Yes | Item Description | Descripción del artículo |
| 15 | `ItemGroupCode` | Edm.Int32 | Yes | Item Group Code | Código de grupo de artículos |
| 16 | `Status` | Edm.Int32 | Yes | Status | Estado |
| 17 | `Priority` | [BoSvcCallPriorities](../Enums/BoSvcCallPriorities.md) | Yes | Priority | Prioridad |
| 18 | `CallType` | Edm.Int32 | Yes | Call Type | Tipo de llamada |
| 19 | `ProblemType` | Edm.Int32 | Yes | Problem Type | Tipo de problema |
| 20 | `AssigneeCode` | Edm.Int32 | Yes | Assignee Code | Código del asignado |
| 21 | `Description` | Edm.String | Yes | Description | Descripción |
| 22 | `TechnicianCode` | Edm.Int32 | Yes | Technician Code | Código del técnico |
| 23 | `Resolution` | Edm.String | Yes | Resolution | Resolución |
| 24 | `CreationDate` | Edm.DateTimeOffset | Yes | Creation Date | Fecha de creación |
| 25 | `CreationTime` | Edm.TimeOfDay | Yes | Creation Time | Hora de creación |
| 26 | `Responder` | Edm.Int32 | Yes | Responder | Respondedor |
| 27 | `UpdatedTime` | Edm.TimeOfDay | Yes | Updated Time | Hora de actualización |
| 28 | `BelongsToAQueue` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Belongs To A Queue | Pertenece a una cola |
| 29 | `ResponseByTime` | Edm.TimeOfDay | Yes | Response By Time | Responder antes de la hora |
| 30 | `ResponseByDate` | Edm.DateTimeOffset | Yes | Response By Date | Responder antes de la fecha |
| 31 | `ResolutionOnDate` | Edm.DateTimeOffset | Yes | Resolution On Date | Resolución en fecha |
| 32 | `ResponseOnTime` | Edm.TimeOfDay | Yes | Response On Time | Respuesta a tiempo |
| 33 | `ResponseOnDate` | Edm.DateTimeOffset | Yes | Response On Date | Respuesta en fecha |
| 34 | `ClosingTime` | Edm.TimeOfDay | Yes | Closing Time | Hora de cierre |
| 35 | `AssignedDate` | Edm.DateTimeOffset | Yes | Assigned Date | Fecha de asignación |
| 36 | `Queue` | Edm.String | Yes | Queue | Cola |
| 37 | `ResponseAssignee` | Edm.Int32 | Yes | Response Assignee | Asignado de la respuesta |
| 38 | `EntitledforService` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Entitledfor Service | Con derecho a servicio |
| 39 | `ResolutionOnTime` | Edm.TimeOfDay | Yes | Resolution On Time | Resolución a tiempo |
| 40 | `AssignedTime` | Edm.TimeOfDay | Yes | Assigned Time | Hora de asignación |
| 41 | `ClosingDate` | Edm.DateTimeOffset | Yes | Closing Date | Fecha de cierre |
| 42 | `Series` | Edm.Int32 | Yes | Series | Serie de numeración |
| 43 | `DocNum` | Edm.Int32 | Yes | Document Number | Número de documento |
| 44 | `HandWritten` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Hand Written | Manual (numeración manual) |
| 45 | `PeriodIndicator` | Edm.String | Yes | Period Indicator | Indicador de período |
| 46 | `StartDate` | Edm.DateTimeOffset | Yes | Start Date | Fecha de inicio |
| 47 | `StartTime` | Edm.TimeOfDay | Yes | Start Time | Hora de inicio |
| 48 | `EndDueDate` | Edm.DateTimeOffset | Yes | End Due Date | Fecha de vencimiento final |
| 49 | `EndTime` | Edm.TimeOfDay | Yes | End Time | Hora de fin |
| 50 | `Duration` | Edm.Double | Yes | Duration | Duración |
| 51 | `DurationType` | [BoDurations](../Enums/BoDurations.md) | Yes | Duration Type | Tipo de duración |
| 52 | `Reminder` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Reminder | Recordatorio |
| 53 | `ReminderPeriod` | Edm.Double | Yes | Reminder Period | Período del recordatorio |
| 54 | `ReminderType` | [BoDurations](../Enums/BoDurations.md) | Yes | Reminder Type | Tipo de recordatorio |
| 55 | `Location` | Edm.Int32 | Yes | Location | Ubicación |
| 56 | `AddressName` | Edm.String | Yes | Address Name | Nombre de dirección |
| 57 | `AddressType` | [BoAddressType](../Enums/BoAddressType.md) | Yes | Address Type | Tipo de dirección |
| 58 | `Street` | Edm.String | Yes | Street | Calle |
| 59 | `City` | Edm.String | Yes | City | Ciudad |
| 60 | `Room` | Edm.String | Yes | Room | Sala/oficina |
| 61 | `State` | Edm.String | Yes | State | Estado/provincia |
| 62 | `Country` | Edm.String | Yes | Country | País |
| 63 | `DisplayInCalendar` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Display In Calendar | Mostrar en calendario |
| 64 | `CustomerRefNo` | Edm.String | Yes | Customer Ref Number | N.º de referencia del cliente |
| 65 | `ProblemSubType` | Edm.Int32 | Yes | Problem Sub Type | Subtipo de problema |
| 66 | `AttachmentEntry` | Edm.Int32 | Yes | Attachment Entry | Entrada de anexo (ID) |
| 67 | `ServiceBPType` | [ServiceTypeEnum](../Enums/ServiceTypeEnum.md) | Yes | Service Business Partner Type | Tipo de socio de negocios del servicio |
| 68 | `BPContactPerson` | Edm.String | Yes | Business Partner Contact Person | Persona de contacto del socio de negocios |
| 69 | `BPPhone1` | Edm.String | Yes | Business Partner Phone 1 | Teléfono 1 del socio de negocios |
| 70 | `BPPhone2` | Edm.String | Yes | Business Partner Phone 2 | Teléfono 2 del socio de negocios |
| 71 | `BPCellular` | Edm.String | Yes | Business Partner Cellular | Celular del socio de negocios |
| 72 | `BPFax` | Edm.String | Yes | Business Partner Fax | Fax del socio de negocios |
| 73 | `BPeMail` | Edm.String | Yes | B Pe Mail | Correo electrónico del socio de negocios |
| 74 | `BPProjectCode` | Edm.String | Yes | Business Partner Project Code | Código de proyecto del socio de negocios |
| 75 | `BPTerritory` | Edm.Int32 | Yes | Business Partner Territory | Territorio del socio de negocios |
| 76 | `BPShipToCode` | Edm.String | Yes | Business Partner Ship To Code | Código de dirección de envío del socio de negocios |
| 77 | `BPShipToAddress` | Edm.String | Yes | Business Partner Ship To Address | Dirección de envío del socio de negocios |
| 78 | `BPBillToCode` | Edm.String | Yes | Business Partner Bill To Code | Código de dirección de facturación del socio de negocios |
| 79 | `BPBillToAddress` | Edm.String | Yes | Business Partner Bill To Address | Dirección de facturación del socio de negocios |
| 80 | `Telephone` | Edm.String | Yes | Telephone | Teléfono |
| 81 | `UpdateDate` | Edm.DateTimeOffset | Yes | Update Date | Fecha de actualización |
| 82 | `SupplementaryCode` | Edm.String | Yes | Supplementary Code | Código complementario |
| 83 | `ServiceCallActivities` | Collection([ServiceCallActivity](../Tipos-Complejos/ServiceCallActivity.md)) | Yes | Service Call Activities | Actividades de la llamada de servicio |
| 84 | `ServiceCallInventoryExpenses` | Collection([ServiceCallInventoryExpense](../Tipos-Complejos/ServiceCallInventoryExpense.md)) | Yes | Service Call Inventory Expenses | Gastos de inventario de la llamada de servicio |
| 85 | `ServiceCallSolutions` | Collection([ServiceCallSolution](../Tipos-Complejos/ServiceCallSolution.md)) | Yes | Service Call Solutions | Soluciones de la llamada de servicio |
| 86 | `ServiceCallSchedulings` | Collection([ServiceCallScheduling](../Tipos-Complejos/ServiceCallScheduling.md)) | Yes | Service Call Schedulings | Programaciones de la llamada de servicio |
| 87 | `ServiceCallBPAddressComponents` | Collection([ServiceCallBPAddressComponent](../Tipos-Complejos/ServiceCallBPAddressComponent.md)) | Yes | Service Call Business Partner Address Components | Componentes de dirección del socio de negocios de la llamada |

## Navigation properties (15)

Use `GET /b1s/v2/ServiceCalls(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `BusinessPartner` | [BusinessPartner](../Entidades/BusinessPartners.md) | [BusinessPartners](BusinessPartners.md) | CustomerCode → CardCode | Socio de negocios |
| `ServiceContract` | [ServiceContract](../Entidades/ServiceContracts.md) | [ServiceContracts](ServiceContracts.md) | ContractID → ContractID | Contratos de servicio |
| `ServiceCallOrigin` | [ServiceCallOrigin](../Entidades/ServiceCallOrigins.md) | [ServiceCallOrigins](ServiceCallOrigins.md) | Origin → OriginID | Orígenes de llamadas de servicio |
| `Item` | [Item](../Entidades/Items.md) | [Items](Items.md) | ItemCode → ItemCode | Artículos |
| `ItemGroups` | [ItemGroups](../Entidades/ItemGroups.md) | [ItemGroups](ItemGroups.md) | ItemGroupCode → Number | Grupos de artículos |
| `ServiceCallStatus` | [ServiceCallStatus](../Entidades/ServiceCallStatus.md) | [ServiceCallStatus](ServiceCallStatus.md) | Status → StatusId | Estados de llamadas de servicio |
| `ServiceCallType` | [ServiceCallType](../Entidades/ServiceCallTypes.md) | [ServiceCallTypes](ServiceCallTypes.md) | CallType → CallTypeID | Tipos de llamadas de servicio |
| `ServiceCallProblemType` | [ServiceCallProblemType](../Entidades/ServiceCallProblemTypes.md) | [ServiceCallProblemTypes](ServiceCallProblemTypes.md) | ProblemType → ProblemTypeID | Tipos de problema de llamadas de servicio |
| `User` | [User](../Entidades/Users.md) | [Users](Users.md) | AssigneeCode → InternalKey | Usuario |
| `EmployeeInfo` | [EmployeeInfo](../Entidades/EmployeesInfo.md) | [EmployeesInfo](EmployeesInfo.md) | TechnicianCode → EmployeeID | Empleados |
| `Queue2` | [Queue](../Entidades/Queue.md) | [Queue](Queue.md) | Queue → QueueID | Colas |
| `ActivityLocation` | [ActivityLocation](../Entidades/ActivityLocations.md) | [ActivityLocations](ActivityLocations.md) | Location → Code | Lugares de actividades |
| `Country2` | [Country](../Entidades/Countries.md) | [Countries](Countries.md) | Country → Code | Países/Regiones |
| `ServiceCallProblemSubType` | [ServiceCallProblemSubType](../Entidades/ServiceCallProblemSubTypes.md) | [ServiceCallProblemSubTypes](ServiceCallProblemSubTypes.md) | ProblemSubType → ProblemSubTypeID | Subtipos de problema de llamadas de servicio |
| `Project` | [Project](../Entidades/Projects.md) | [Projects](Projects.md) | BPProjectCode → Code | Proyecto |

## Bound actions (1)

### Close

- **Descripción (ES):** Cerrar
- **Request:** `POST /b1s/v2/ServiceCalls(1)/Close`

