# ProjectManagementTimeSheet — Hojas de horas de gestión de proyectos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `ProjectManagementTimeSheet`
- **Descripción (ES):** Hojas de horas de gestión de proyectos
- **Entity type:** `PM_TimeSheetData` (open type: accepts dynamic/UDF properties)
- **Key:** `AbsEntry` (Edm.Int32)
- **DB tables (main / lines):** [OTSH](../../Tablas%20SAP%20B1/OTSH.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 14 · **Navigation properties:** 2 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/ProjectManagementTimeSheet?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/ProjectManagementTimeSheet/$count` | Contar |
| Get by key | `GET /b1s/v2/ProjectManagementTimeSheet(1)` | Obtener por clave |
| Create | `POST /b1s/v2/ProjectManagementTimeSheet` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/ProjectManagementTimeSheet(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/ProjectManagementTimeSheet(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/ProjectManagementTimeSheet(1)` (only if the B1 object allows removal) | Borrar |

## Properties (14)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` 🔑 | Edm.Int32 | No | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `DocNumber` | Edm.Int32 | Yes | Document Number | Número de documento |
| 3 | `TimeSheetType` | [TimeSheetTypeEnum](../Enums/TimeSheetTypeEnum.md) | Yes | Time Sheet Type | Tipo de hoja de horas |
| 4 | `UserID` | Edm.Int32 | Yes | User ID | ID de usuario |
| 5 | `LastName` | Edm.String | Yes | Last Name | Apellido |
| 6 | `FirstName` | Edm.String | Yes | First Name | Nombre |
| 7 | `Department` | Edm.Int32 | Yes | Department | Departamento |
| 8 | `OwnerCode` | Edm.Int32 | Yes | Owner Code | Código del titular |
| 9 | `DateFrom` | Edm.DateTimeOffset | Yes | Date From | Fecha desde |
| 10 | `DateTo` | Edm.DateTimeOffset | Yes | Date To | Fecha hasta |
| 11 | `SAPPassport` | Edm.String | Yes | SAP Passport | SAP Passport |
| 12 | `AttachmentEntry` | Edm.Int32 | Yes | Attachment Entry | Entrada de anexo (ID) |
| 13 | `UserCode` | Edm.String | Yes | User Code | Código de usuario |
| 14 | `PM_TimeSheetLineDataCollection` | Collection([PM_TimeSheetLineData](../Tipos-Complejos/PM_TimeSheetLineData.md)) | Yes | PM Time Sheet Line Data Collection | Colección de líneas de hoja de horas |

## Navigation properties (2)

Use `GET /b1s/v2/ProjectManagementTimeSheet(1)/<Navigation>` or `$expand=<Navigation>`.

| Navigation | Target type | Target entity set | Join (local → target) | Descripción (ES) |
|---|---|---|---|---|
| `EmployeeInfo` | [EmployeeInfo](../Entidades/EmployeesInfo.md) | [EmployeesInfo](EmployeesInfo.md) | UserID → EmployeeID | Empleados |
| `Attachments2` | [Attachments2](../Entidades/Attachments2.md) | [Attachments2](Attachments2.md) | AttachmentEntry → AbsoluteEntry | Anexos |
