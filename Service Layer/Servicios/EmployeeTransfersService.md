# EmployeeTransfersService — Servicio de transferencias de empleados

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `EmployeeTransfersService`
- **Descripción (ES):** Servicio de transferencias de empleados
- **Operations:** 1

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`EmployeeTransfersService_GetEmployeeTransferList`](#employeetransfersservice_getemployeetransferlist) | action | Collection([EmployeeTransferParams](../Tipos-Complejos/EmployeeTransferParams.md)) | Get Employee Transfer List | Obtener lista de transferencias de empleados |

## EmployeeTransfersService_GetEmployeeTransferList

- **Descripción (ES):** Obtener lista de transferencias de empleados
- **Request:** `POST /b1s/v2/EmployeeTransfersService_GetEmployeeTransferList`
- **Parameters:** none
- **Returns:** Collection([EmployeeTransferParams](../Tipos-Complejos/EmployeeTransferParams.md))

