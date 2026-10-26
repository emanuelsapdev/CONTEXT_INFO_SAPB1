# EmployeeTransferDetail — Detalles de transferencia del empleado

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EmployeeTransferDetail`
- **Descripción (ES):** Detalles de transferencia del empleado
- **Description (EN):** Employee Transfer Detail

- **Properties:** 6

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TransferID` | Edm.Int32 | Yes | Transfer ID | ID de transferencia |
| 2 | `EmployeeID` | Edm.Int32 | Yes | Employee ID | ID de empleado |
| 3 | `TransferedDate` | Edm.DateTimeOffset | Yes | Transfered Date | Fecha de transferencia |
| 4 | `TransferedTime` | Edm.TimeOfDay | Yes | Transfered Time | Hora de transferencia |
| 5 | `Status` | [EmployeeTransferProcessingStatusEnum](../Enums/EmployeeTransferProcessingStatusEnum.md) | Yes | Status | Estado |
| 6 | `Comment` | Edm.String | Yes | Comment | Comentario |

## Used by (properties)

- [EmployeeTransfer](../Entidades/EmployeeTransfers.md).`EmployeeTransferDetails`
