# AlertManagements — Gestión de alertas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `AlertManagements`
- **Descripción (ES):** Gestión de alertas
- **Entity type:** `AlertManagement` (open type: accepts dynamic/UDF properties)
- **Key:** `Code` (Edm.Int32)
- **DB tables (main / lines):** [OALT](../../Tablas%20SAP%20B1/OALT.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 18 · **Navigation properties:** 0 · **Bound actions:** 1

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/AlertManagements?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/AlertManagements/$count` | Contar |
| Get by key | `GET /b1s/v2/AlertManagements(1)` | Obtener por clave |
| Create | `POST /b1s/v2/AlertManagements` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/AlertManagements(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/AlertManagements(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/AlertManagements(1)` (only if the B1 object allows removal) | Borrar |
| Action `GetAlertManagementList` | `POST /b1s/v2/AlertManagements(1)/GetAlertManagementList` | Obtener lista de gestión de alertas |

## Properties (18)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Code` 🔑 | Edm.Int32 | No | Code | Código |
| 2 | `Name` | Edm.String | Yes | Name | Nombre |
| 3 | `Type` | [AlertManagementTypeEnum](../Enums/AlertManagementTypeEnum.md) | Yes | Type | Tipo |
| 4 | `Priority` | [AlertManagementPriorityEnum](../Enums/AlertManagementPriorityEnum.md) | Yes | Priority | Prioridad |
| 5 | `Active` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Active | Activo |
| 6 | `Param` | Edm.String | Yes | Parameter | Parámetro |
| 7 | `QueryID` | Edm.Int32 | Yes | Query ID | ID de consulta |
| 8 | `FrequencyType` | [AlertManagementFrequencyType](../Enums/AlertManagementFrequencyType.md) | Yes | Frequency Type | Tipo de frecuencia |
| 9 | `DayOfExecution` | Edm.Int32 | Yes | Day Of Execution | Día de ejecución |
| 10 | `ExecutionTime` | Edm.TimeOfDay | Yes | Execution Time | Hora de ejecución |
| 11 | `LastExecutionDate` | Edm.DateTimeOffset | Yes | Last Execution Date | Fecha de última ejecución |
| 12 | `LastExecutionTime` | Edm.Int32 | Yes | Last Execution Time | Hora de última ejecución |
| 13 | `NextExecutionDate` | Edm.DateTimeOffset | Yes | Next Execution Date | Fecha de la siguiente ejecución |
| 14 | `NextExecutionTime` | Edm.TimeOfDay | Yes | Next Execution Time | Hora de la siguiente ejecución |
| 15 | `SaveHistory` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Save History | Guardar historial |
| 16 | `FrequencyInterval` | Edm.Int32 | Yes | Frequency Interval | Intervalo de frecuencia |
| 17 | `AlertManagementRecipients` | Collection([AlertManagementRecipient](../Tipos-Complejos/AlertManagementRecipient.md)) | Yes | Alert Management Recipients | Destinatarios de la gestión de alertas |
| 18 | `AlertManagementDocuments` | Collection([AlertManagementDocument](../Tipos-Complejos/AlertManagementDocument.md)) | Yes | Alert Management Documents | Documentos de la gestión de alertas |

## Bound actions (1)

### GetAlertManagementList

- **Descripción (ES):** Obtener lista de gestión de alertas
- **Request:** `POST /b1s/v2/AlertManagements(1)/GetAlertManagementList`
- **Returns:** Collection([AlertManagementParams](../Tipos-Complejos/AlertManagementParams.md))

