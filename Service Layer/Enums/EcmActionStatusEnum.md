# EcmActionStatusEnum — Estado de acción ECM

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `EcmActionStatusEnum`
- **Descripción (ES):** Estado de acción ECM
- **Underlying type:** Edm.Int32
- **Members:** 16

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `lasNone` | 0 | None | Ninguno |
| `lasNew` | 1 | New | Nuevo |
| `lasPending` | 2 | Pending | Pendiente |
| `lasError` | 3 | Error | Error |
| `lasOK` | 4 | OK | Correcto |
| `lasSent` | 5 | Sent | Enviado |
| `lasDocError` | 6 | Document Error | Error en el documento |
| `lasWaiting` | 7 | Waiting | En espera |
| `lasAuthorized` | 8 | Authorized | Autorizado |
| `lasInProcess` | 9 | In Process | En proceso |
| `lasRejected` | 10 | Rejected | Rechazado |
| `lasDenied` | 11 | Denied | Denegado |
| `lasCanceled` | 12 | Canceled | Cancelado |
| `lasAborted` | 13 | Aborted | Abortado |
| `lasQueued` | 14 | Queued | En cola |
| `lasImported` | 15 | Imported | Importado |

## Used by (3 properties)

- [AFEFceActionGetByFceID](../Tipos-Complejos/AFEFceActionGetByFceID.md).`ActStatus`
- [ECMActionStatusData](../Tipos-Complejos/ECMActionStatusData.md).`ActStatus`
- [EcmAction](../Tipos-Complejos/EcmAction.md).`Status`
