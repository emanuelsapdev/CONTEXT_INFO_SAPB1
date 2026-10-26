# ProjectManagements — Gestión de proyectos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ProjectManagements`
- **Descripción (ES):** Gestión de proyectos
- **Entity type:** `PM_ProjectDocumentData` (open type: accepts dynamic/UDF properties)
- **Key:** `AbsEntry` (Edm.Int32)
- **DB tables (main / lines):** [OPMG](../../Tablas%20SAP%20B1/OPMG.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 30 · **Navigation properties:** 7 · **Bound actions:** 1

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ProjectManagements?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ProjectManagements/$count` | Contar |
| Get by key | `GET /b1s/v2/ProjectManagements(1)` | Obtener por clave |
| Create | `POST /b1s/v2/ProjectManagements` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ProjectManagements(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ProjectManagements(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/ProjectManagements(1)` (only if the B1 object allows removal) | Borrar |
| Action `CancelProject` | `POST /b1s/v2/ProjectManagements(1)/CancelProject` | Cancelar proyecto |

## Properties (30)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` 🔑 | Edm.Int32 | No | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `Owner` | Edm.Int32 | Yes | Owner | Titular |
| 3 | `ProjectName` | Edm.String | Yes | Project Name | Nombre del proyecto |
| 4 | `StartDate` | Edm.DateTimeOffset | Yes | Start Date | Fecha de inicio |
| 5 | `FinishedPercent` | Edm.Double | Yes | Finished Percent | Porcentaje completado |
| 6 | `DocNum` | Edm.Int32 | Yes | Document Number | Número de documento |
| 7 | `Series` | Edm.Int32 | Yes | Series | Serie de numeración |
| 8 | `ProjectType` | [ProjectTypeEnum](../Enums/ProjectTypeEnum.md) | Yes | Project Type | Tipo de proyecto |
| 9 | `BusinessPartner` | Edm.String | Yes | Business Partner | Socio de negocios |
| 10 | `BusinessPartnerName` | Edm.String | Yes | Business Partner Name | Nombre del socio de negocios |
| 11 | `ContactPerson` | Edm.Int32 | Yes | Contact Person | Persona de contacto |
| 12 | `Territory` | Edm.Int32 | Yes | Territory | Territorio |
| 13 | `SalesEmployee` | Edm.Int32 | Yes | Sales Employee | Empleado de ventas |
| 14 | `AllowSubprojects` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Allow Subprojects | Permitir subproyectos |
| 15 | `ProjectStatus` | [ProjectStatusTypeEnum](../Enums/ProjectStatusTypeEnum.md) | Yes | Project Status | Estado del proyecto |
| 16 | `DueDate` | Edm.DateTimeOffset | Yes | Due Date | Fecha de vencimiento |
| 17 | `ClosingDate` | Edm.DateTimeOffset | Yes | Closing Date | Fecha de cierre |
| 18 | `FinancialProject` | Edm.String | Yes | Financial Project | Proyecto financiero |
| 19 | `RiskLevel` | [RiskLevelTypeEnum](../Enums/RiskLevelTypeEnum.md) | Yes | Risk Level | Nivel de riesgo |
| 20 | `Industry` | Edm.Int32 | Yes | Industry | Ramo (industria) |
| 21 | `Reason` | Edm.String | Yes | Reason | Motivo |
| 22 | `AttachmentEntry` | Edm.Int32 | Yes | Attachment Entry | Entrada de anexo (ID) |
| 23 | `PM_StagesCollection` | Collection([PM_StageData](../Tipos-Complejos/PM_StageData.md)) | Yes | PM Stages Collection | Colección de etapas del proyecto |
| 24 | `PM_OpenIssuesCollection` | Collection([PM_OpenIssueData](../Tipos-Complejos/PM_OpenIssueData.md)) | Yes | PM Open Issues Collection | Colección de temas abiertos del proyecto |
| 25 | `PM_DocumentsCollection` | Collection([PM_DocumentData](../Tipos-Complejos/PM_DocumentData.md)) | Yes | PM Documents Collection | Colección de documentos del proyecto |
| 26 | `PM_ActivitiesCollection` | Collection([PM_ActivityData](../Tipos-Complejos/PM_ActivityData.md)) | Yes | PM Activities Collection | Colección de actividades del proyecto |
| 27 | `PM_WorkOrdersCollection` | Collection([PM_WorkOrderData](../Tipos-Complejos/PM_WorkOrderData.md)) | Yes | PM Work Orders Collection | Colección de órdenes de trabajo del proyecto |
| 28 | `PM_SummaryData` | [PM_SummaryData](../Tipos-Complejos/PM_SummaryData.md) | Yes | PM Summary Data | Datos de resumen del proyecto |
| 29 | `PM_DocAttachements` | Collection([PM_DocAttachement](../Tipos-Complejos/PM_DocAttachement.md)) | Yes | PM Document Attachements | Anexos del documento del proyecto |
| 30 | `PM_StageAttachements` | Collection([PM_StageAttachement](../Tipos-Complejos/PM_StageAttachement.md)) | Yes | PM Stage Attachements | Anexos de etapas del proyecto |

## Navigation properties (7)

Use `GET /b1s/v2/ProjectManagements(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `EmployeeInfo` | [EmployeeInfo](../Entidades/EmployeesInfo.md) | [EmployeesInfo](EmployeesInfo.md) | Owner → EmployeeID | Empleados |
| `BusinessPartner2` | [BusinessPartner](../Entidades/BusinessPartners.md) | [BusinessPartners](BusinessPartners.md) | BusinessPartner → CardCode | Socios de negocios |
| `Territory2` | [Territory](../Entidades/Territories.md) | [Territories](Territories.md) | Territory → TerritoryID | Territorios |
| `SalesPerson` | [SalesPerson](../Entidades/SalesPersons.md) | [SalesPersons](SalesPersons.md) | SalesEmployee → SalesEmployeeCode | Empleado de ventas |
| `Project` | [Project](../Entidades/Projects.md) | [Projects](Projects.md) | FinancialProject → Code | Proyecto |
| `Industry2` | [Industry](../Entidades/Industries.md) | [Industries](Industries.md) | Industry → IndustryCode | Ramos (industrias) |
| `Attachments2` | [Attachments2](../Entidades/Attachments2.md) | [Attachments2](Attachments2.md) | AttachmentEntry → AbsoluteEntry | Anexos |

## Bound actions (1)

### CancelProject

- **Descripción (ES):** Cancelar proyecto
- **Request:** `POST /b1s/v2/ProjectManagements(1)/CancelProject`

