# ContractTemplates — Plantillas de contrato

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ContractTemplates`
- **Descripción (ES):** Plantillas de contrato
- **Entity type:** `ContractTemplate` (open type: accepts dynamic/UDF properties)
- **Key:** `TemplateName` (Edm.String)
- **DB tables (main / lines):** [OCTT](../../Tablas%20SAP%20B1/OCTT.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 39 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ContractTemplates?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ContractTemplates/$count` | Contar |
| Get by key | `GET /b1s/v2/ContractTemplates('value')` | Obtener por clave |
| Create | `POST /b1s/v2/ContractTemplates` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ContractTemplates('value')` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ContractTemplates('value')` | Reemplazar |
| Delete | `DELETE /b1s/v2/ContractTemplates('value')` (only if the B1 object allows removal) | Borrar |

## Properties (39)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TemplateName` 🔑 | Edm.String | No | Template Name | Nombre de la plantilla |
| 2 | `TemplateIsDeleted` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Template Is Deleted | Plantilla eliminada |
| 3 | `TemplateIsRenewal` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Template Is Renewal | Plantilla de renovación |
| 4 | `RemindBeforeRenewal` | Edm.Int32 | Yes | Remind Before Renewal | Recordar antes de la renovación |
| 5 | `RemindUnit` | [BoRemindUnits](../Enums/BoRemindUnits.md) | Yes | Remind Unit | Unidad de recordatorio |
| 6 | `DurationOfCoverage` | Edm.Int32 | Yes | Duration Of Coverage | Duración de la cobertura |
| 7 | `ResponseValue` | Edm.Int32 | Yes | Response Value | Valor de respuesta |
| 8 | `ResolutionUnit` | [BoResolutionUnits](../Enums/BoResolutionUnits.md) | Yes | Resolution Unit | Unidad de tiempo de resolución |
| 9 | `Description` | Edm.String | Yes | Description | Descripción |
| 10 | `ContractType` | [BoContractTypes](../Enums/BoContractTypes.md) | Yes | Contract Type | Tipo de contrato |
| 11 | `MondayEnabled` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Monday Enabled | Lunes habilitado |
| 12 | `TuesdayEnabled` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Tuesday Enabled | Martes habilitado |
| 13 | `WednesdayEnabled` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Wednesday Enabled | Miércoles habilitado |
| 14 | `ThursdayEnabled` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Thursday Enabled | Jueves habilitado |
| 15 | `FridayEnabled` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Friday Enabled | Viernes habilitado |
| 16 | `SaturdayEnabled` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Saturday Enabled | Sábado habilitado |
| 17 | `SundayEnabled` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Sunday Enabled | Domingo habilitado |
| 18 | `MondayStart` | Edm.TimeOfDay | Yes | Monday Start | Inicio del lunes |
| 19 | `MondayEnd` | Edm.TimeOfDay | Yes | Monday End | Fin del lunes |
| 20 | `TuesdayStart` | Edm.TimeOfDay | Yes | Tuesday Start | Inicio del martes |
| 21 | `TuesdayEnd` | Edm.TimeOfDay | Yes | Tuesday End | Fin del martes |
| 22 | `WednesdayStart` | Edm.TimeOfDay | Yes | Wednesday Start | Inicio del miércoles |
| 23 | `WednesdayEnd` | Edm.TimeOfDay | Yes | Wednesday End | Fin del miércoles |
| 24 | `ThursdayStart` | Edm.TimeOfDay | Yes | Thursday Start | Inicio del jueves |
| 25 | `ThursdayEnd` | Edm.TimeOfDay | Yes | Thursday End | Fin del jueves |
| 26 | `FridayStart` | Edm.TimeOfDay | Yes | Friday Start | Inicio del viernes |
| 27 | `FridayEnd` | Edm.TimeOfDay | Yes | Friday End | Fin del viernes |
| 28 | `SaturdayStart` | Edm.TimeOfDay | Yes | Saturday Start | Inicio del sábado |
| 29 | `SaturdayEnd` | Edm.TimeOfDay | Yes | Saturday End | Fin del sábado |
| 30 | `SundayStart` | Edm.TimeOfDay | Yes | Sunday Start | Inicio del domingo |
| 31 | `SundayEnd` | Edm.TimeOfDay | Yes | Sunday End | Fin del domingo |
| 32 | `IncludeParts` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Include Parts | Incluir repuestos |
| 33 | `IncludeLabor` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Include Labor | Incluir mano de obra |
| 34 | `IncludeTravel` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Include Travel | Incluir viajes |
| 35 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 36 | `IncludeHolidays` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Include Holidays | Incluir festivos |
| 37 | `ResponseUnit` | [BoResponseUnit](../Enums/BoResponseUnit.md) | Yes | Response Unit | Unidad de tiempo de respuesta |
| 38 | `ResolutionTime` | Edm.Int32 | Yes | Resolution Time | Tiempo de resolución |
| 39 | `AttachmentEntry` | Edm.Int32 | Yes | Attachment Entry | Entrada de anexo (ID) |

## Navigation properties (2)

Use `GET /b1s/v2/ContractTemplates('value')/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `Items` | Collection([Item](../Entidades/Items.md)) | [Items](Items.md) |  | Artículos |
| `ServiceContracts` | Collection([ServiceContract](../Entidades/ServiceContracts.md)) | [ServiceContracts](ServiceContracts.md) |  | Contratos de servicio |
