# ElectronicDocumentEntryCancellationStatusEnum — Estado de cancelación del documento electrónico

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ElectronicDocumentEntryCancellationStatusEnum`
- **Descripción (ES):** Estado de cancelación del documento electrónico
- **Underlying type:** Edm.Int32
- **Members:** 11

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `edecsInvalid` | 0 | Invalid | Inválido |
| `edecsNotSet` | 1 | Not Set | No establecido |
| `edecsNewRequest` | 2 | New Request | Nueva solicitud |
| `edecsRequestSent` | 3 | Request Sent | Solicitud enviada |
| `edecsApproved` | 4 | Approved | Aprobado |
| `edecsRejected` | 5 | Rejected | Rechazado |
| `edecsError` | 6 | Error | Error |
| `edecsCancelled` | 7 | Cancelled | Cancelado |
| `edecsInProcess` | 8 | In Process | En proceso |
| `edecsSentToAuthority` | 9 | Sent To Authority | Enviado a la autoridad |
| `edescCancelledWOApproval` | 10 | Cancelled WO Approval | Cancelado sin aprobación |

## Used by (1 properties)

- [EDFEntry](../Tipos-Complejos/EDFEntry.md).`CancellationStatus`
