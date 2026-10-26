# EmployeeTransfers — Transferencias de empleados

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Entity set:** `EmployeeTransfers`
- **Descripción (ES):** Transferencias de empleados
- **Entity type:** `EmployeeTransfer`
- **Key:** `TransferID` (Edm.Int32)
- **DB tables (main / lines):** [OHET](../../Tablas%20SAP%20B1/OHET.md)
- **ETag / optimistic concurrency:** No

- **Properties:** 8 · **Navigation properties:** 0 · **Bound actions:** 0

## Endpoints

| Operation | Request | Operación (ES) |
|---|---|---|
| List / query | `GET /b1s/v2/EmployeeTransfers?$select=...&$filter=...&$orderby=...&$top=...&$skip=...` | Listar / consultar |
| Count | `GET /b1s/v2/EmployeeTransfers/$count` | Contar |
| Get by key | `GET /b1s/v2/EmployeeTransfers(1)` | Obtener por clave |
| Create | `POST /b1s/v2/EmployeeTransfers` + JSON body | Crear |
| Update (partial) | `PATCH /b1s/v2/EmployeeTransfers(1)` + changed fields | Actualizar (parcial) |
| Replace | `PUT /b1s/v2/EmployeeTransfers(1)` | Reemplazar |
| Delete | `DELETE /b1s/v2/EmployeeTransfers(1)` (only if the B1 object allows removal) | Borrar |

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TransferID` 🔑 | Edm.Int32 | No | Transfer ID | ID de transferencia |
| 2 | `TransStartDate` | Edm.DateTimeOffset | Yes | Trans Start Date | Fecha de inicio del transporte |
| 3 | `TransStartTime` | Edm.TimeOfDay | Yes | Trans Start Time | Hora de inicio del transporte |
| 4 | `TransEndDate` | Edm.DateTimeOffset | Yes | Trans End Date | Fecha de fin del transporte |
| 5 | `TransEndTime` | Edm.TimeOfDay | Yes | Trans End Time | Hora de fin del transporte |
| 6 | `Status` | [EmployeeTransferStatusEnum](../Enums/EmployeeTransferStatusEnum.md) | Yes | Status | Estado |
| 7 | `Comment` | Edm.String | Yes | Comment | Comentario |
| 8 | `EmployeeTransferDetails` | Collection([EmployeeTransferDetail](../Tipos-Complejos/EmployeeTransferDetail.md)) | Yes | Employee Transfer Details | Detalles de transferencia del empleado |
