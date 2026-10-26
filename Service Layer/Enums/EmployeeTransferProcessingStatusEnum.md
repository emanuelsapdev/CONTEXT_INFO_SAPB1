# EmployeeTransferProcessingStatusEnum — Estado de procesamiento de la transferencia de empleado

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `EmployeeTransferProcessingStatusEnum`
- **Descripción (ES):** Estado de procesamiento de la transferencia de empleado
- **Underlying type:** Edm.Int32
- **Members:** 4

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `etps_New` | 0 | New | Nuevo |
| `etps_Sent` | 1 | Sent | Enviado |
| `etps_Accepted` | 2 | Accepted | Aceptado |
| `etps_Error` | 3 | Error | Error |

## Used by (1 properties)

- [EmployeeTransferDetail](../Tipos-Complejos/EmployeeTransferDetail.md).`Status`
