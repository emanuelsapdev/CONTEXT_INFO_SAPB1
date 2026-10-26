# ServiceContracts — Contratos de servicio

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ServiceContracts`
- **Descripción (ES):** Contratos de servicio
- **Entity type:** `ServiceContract` (open type: accepts dynamic/UDF properties)
- **Key:** `ContractID` (Edm.Int32)
- **DB tables (main / lines):** [OCTR](../../Tablas%20SAP%20B1/OCTR.md), [CTR1](../../Tablas%20SAP%20B1/CTR1.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 51 · **Navigation properties:** 6 · **Bound actions:** 2

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ServiceContracts?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ServiceContracts/$count` | Contar |
| Get by key | `GET /b1s/v2/ServiceContracts(1)` | Obtener por clave |
| Create | `POST /b1s/v2/ServiceContracts` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ServiceContracts(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ServiceContracts(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/ServiceContracts(1)` (only if the B1 object allows removal) | Borrar |
| Action `Cancel` | `POST /b1s/v2/ServiceContracts(1)/Cancel` | Cancelar |
| Action `Close` | `POST /b1s/v2/ServiceContracts(1)/Close` | Cerrar |

## Properties (51)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ContractID` 🔑 | Edm.Int32 | No | Contract ID | ID de contrato |
| 2 | `CustomerCode` | Edm.String | Yes | Customer Code | Código de cliente |
| 3 | `CustomerName` | Edm.String | Yes | Customer Name | Nombre del cliente |
| 4 | `ContactCode` | Edm.Int32 | Yes | Contact Code | Código de contacto |
| 5 | `Owner` | Edm.Int32 | Yes | Owner | Titular |
| 6 | `Status` | [BoSvcContractStatus](../Enums/BoSvcContractStatus.md) | Yes | Status | Estado |
| 7 | `ContractTemplate` | Edm.String | Yes | Contract Template | Plantilla de contrato |
| 8 | `ContractType` | [BoContractTypes](../Enums/BoContractTypes.md) | Yes | Contract Type | Tipo de contrato |
| 9 | `Renewal` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Renewal | Renovación |
| 10 | `ReminderTime` | Edm.Int32 | Yes | Reminder Time | Hora del recordatorio |
| 11 | `RemindUnit` | [BoRemindUnits](../Enums/BoRemindUnits.md) | Yes | Remind Unit | Unidad de recordatorio |
| 12 | `DurationOfCoverage` | Edm.Int32 | Yes | Duration Of Coverage | Duración de la cobertura |
| 13 | `StartDate` | Edm.DateTimeOffset | Yes | Start Date | Fecha de inicio |
| 14 | `EndDate` | Edm.DateTimeOffset | Yes | End Date | Fecha de fin |
| 15 | `ResolutionTime` | Edm.Int32 | Yes | Resolution Time | Tiempo de resolución |
| 16 | `ResolutionUnit` | [BoResolutionUnits](../Enums/BoResolutionUnits.md) | Yes | Resolution Unit | Unidad de tiempo de resolución |
| 17 | `Description` | Edm.String | Yes | Description | Descripción |
| 18 | `MondayEnabled` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Monday Enabled | Lunes habilitado |
| 19 | `TuesdayEnabled` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Tuesday Enabled | Martes habilitado |
| 20 | `WednesdayEnabled` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Wednesday Enabled | Miércoles habilitado |
| 21 | `ThursdayEnabled` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Thursday Enabled | Jueves habilitado |
| 22 | `FridayEnabled` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Friday Enabled | Viernes habilitado |
| 23 | `SaturdayEnabled` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Saturday Enabled | Sábado habilitado |
| 24 | `SundayEnabled` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Sunday Enabled | Domingo habilitado |
| 25 | `MondayStart` | Edm.TimeOfDay | Yes | Monday Start | Inicio del lunes |
| 26 | `MondayEnd` | Edm.TimeOfDay | Yes | Monday End | Fin del lunes |
| 27 | `TuesdayStart` | Edm.TimeOfDay | Yes | Tuesday Start | Inicio del martes |
| 28 | `TuesdayEnd` | Edm.TimeOfDay | Yes | Tuesday End | Fin del martes |
| 29 | `WednesdayStart` | Edm.TimeOfDay | Yes | Wednesday Start | Inicio del miércoles |
| 30 | `WednesdayEnd` | Edm.TimeOfDay | Yes | Wednesday End | Fin del miércoles |
| 31 | `ThursdayStart` | Edm.TimeOfDay | Yes | Thursday Start | Inicio del jueves |
| 32 | `ThursdayEnd` | Edm.TimeOfDay | Yes | Thursday End | Fin del jueves |
| 33 | `FridayStart` | Edm.TimeOfDay | Yes | Friday Start | Inicio del viernes |
| 34 | `FridayEnd` | Edm.TimeOfDay | Yes | Friday End | Fin del viernes |
| 35 | `SaturdayStart` | Edm.TimeOfDay | Yes | Saturday Start | Inicio del sábado |
| 36 | `SaturdayEnd` | Edm.TimeOfDay | Yes | Saturday End | Fin del sábado |
| 37 | `SundayStart` | Edm.TimeOfDay | Yes | Sunday Start | Inicio del domingo |
| 38 | `SundayEnd` | Edm.TimeOfDay | Yes | Sunday End | Fin del domingo |
| 39 | `IncludeParts` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Include Parts | Incluir repuestos |
| 40 | `IncludeLabor` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Include Labor | Incluir mano de obra |
| 41 | `IncludeTravel` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Include Travel | Incluir viajes |
| 42 | `TemplateRemarks` | Edm.String | Yes | Template Remarks | Comentarios de la plantilla |
| 43 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 44 | `IncludeHolidays` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Include Holidays | Incluir festivos |
| 45 | `ServiceType` | [BoServiceTypes](../Enums/BoServiceTypes.md) | Yes | Service Type | Tipo de servicio |
| 46 | `ResponseUnit` | [BoResponseUnit](../Enums/BoResponseUnit.md) | Yes | Response Unit | Unidad de tiempo de respuesta |
| 47 | `ResponseTime` | Edm.Int32 | Yes | Response Time | Tiempo de respuesta |
| 48 | `TerminationDate` | Edm.DateTimeOffset | Yes | Termination Date | Fecha de terminación |
| 49 | `AttachmentEntry` | Edm.Int32 | Yes | Attachment Entry | Entrada de anexo (ID) |
| 50 | `ServiceBPType` | [ServiceTypeEnum](../Enums/ServiceTypeEnum.md) | Yes | Service Business Partner Type | Tipo de socio de negocios del servicio |
| 51 | `ServiceContract_Lines` | Collection([ServiceContract_Line](../Tipos-Complejos/ServiceContract_Line.md)) | Yes | Service Contract Lines | Líneas del contrato de servicio |

## Navigation properties (6)

Use `GET /b1s/v2/ServiceContracts(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `CustomerEquipmentCards` | Collection([CustomerEquipmentCard](../Entidades/CustomerEquipmentCards.md)) | [CustomerEquipmentCards](CustomerEquipmentCards.md) |  | Tarjetas de equipo del cliente |
| `ServiceCalls` | Collection([ServiceCall](../Entidades/ServiceCalls.md)) | [ServiceCalls](ServiceCalls.md) |  | Llamadas de servicio |
| `BusinessPartner` | [BusinessPartner](../Entidades/BusinessPartners.md) | [BusinessPartners](BusinessPartners.md) | CustomerCode → CardCode | Socio de negocios |
| `User` | [User](../Entidades/Users.md) | [Users](Users.md) | Owner → InternalKey | Usuario |
| `ContractTemplate2` | [ContractTemplate](../Entidades/ContractTemplates.md) | [ContractTemplates](ContractTemplates.md) | ContractTemplate → TemplateName | Plantillas de contrato |
| `Attachments2` | [Attachments2](../Entidades/Attachments2.md) | [Attachments2](Attachments2.md) | AttachmentEntry → AbsoluteEntry | Anexos |

## Bound actions (2)

### Cancel

- **Descripción (ES):** Cancelar
- **Request:** `POST /b1s/v2/ServiceContracts(1)/Cancel`

### Close

- **Descripción (ES):** Cerrar
- **Request:** `POST /b1s/v2/ServiceContracts(1)/Close`

