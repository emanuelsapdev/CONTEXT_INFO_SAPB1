# ElectronicDocumentEntryStatusEnum — Estado del documento electrónico

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Enum type:** `ElectronicDocumentEntryStatusEnum`
- **Descripción (ES):** Estado del documento electrónico
- **Underlying type:** Edm.Int32
- **Members:** 45

> Service Layer accepts the member **name** (e.g. `tYES`) in JSON payloads and filters; for many enums the stored database value (e.g. `Y`) is also accepted. `Value` below is the OData numeric value.

| Member (name) | Value | Description (EN) | Descripción (ES) |
|---|---|---|---|
| `edesNone` | 0 | None | Ninguno |
| `edesNew` | 1 | New | Nuevo |
| `edesReadyToProcess` | 2 | Ready To Process | Listo para procesar |
| `edesPending` | 3 | Pending | Pendiente |
| `edesError` | 4 | Error | Error |
| `edesOK` | 5 | OK | Correcto |
| `edesSent` | 6 | Sent | Enviado |
| `edesDocError` | 7 | Document Error | Error en el documento |
| `edesTempError` | 8 | Temp Error | Error temporal |
| `edesWarning` | 9 | Warning | Advertencia |
| `edesWaiting` | 10 | Waiting | En espera |
| `edesAuthorized` | 11 | Authorized | Autorizado |
| `edesInProcess` | 12 | In Process | En proceso |
| `edesRejected` | 13 | Rejected | Rechazado |
| `edesDenied` | 14 | Denied | Denegado |
| `edesCanceled` | 15 | Canceled | Cancelado |
| `edesAborted` | 16 | Aborted | Abortado |
| `edesUnused` | 17 | Unused | Sin usar |
| `edesQueued` | 18 | Queued | En cola |
| `edesImported` | 19 | Imported | Importado |
| `edesApproved` | 20 | Approved | Aprobado |
| `edesApproving` | 21 | Approving | Aprobando |
| `edesRejecting` | 22 | Rejecting | Rechazando |
| `edesGenerated` | 23 | Generated | Generado |
| `edesDetermined` | 24 | Determined | Determinado |
| `edesImporting` | 25 | Importing | Importando |
| `edesInProcessToIntermediary` | 26 | In Process To Intermediary | En proceso hacia el intermediario |
| `edesSentToIntermediary` | 27 | Sent To Intermediary | Enviado al intermediario |
| `edesApprovedByIntermediary` | 28 | Approved By Intermediary | Aprobado por el intermediario |
| `edesNotIntegratedCustomer` | 29 | Not Integrated Customer | Cliente no integrado |
| `edesNotSentToCustomer` | 30 | Not Sent To Customer | No enviado al cliente |
| `edesErrorSendingToCustomer` | 31 | Error Sending To Customer | Error al enviar al cliente |
| `edesSentToCustomer` | 32 | Sent To Customer | Enviado al cliente |
| `edesReceivedByCustomer` | 33 | Received By Customer | Recibido por el cliente |
| `edesRejectedByCustomer` | 34 | Rejected By Customer | Rechazado por el cliente |
| `edesPaidByCustomer` | 35 | Paid By Customer | Pagado por el cliente |
| `edesCheckingIntegrationStatus` | 36 | Checking Integration Status | Verificando estado de integración |
| `edesNotApproved` | 37 | Not Approved | No aprobado |
| `edesChargeReversal` | 38 | Charge Reversal | Reversión de cargo |
| `edesCanceling` | 39 | Canceling | Cancelando |
| `edesContinuing` | 40 | Continuing | Continuando |
| `edesContinued` | 41 | Continued | Continuado |
| `edesFurtherObjecting` | 42 | Further Objecting | Objetando nuevamente |
| `edesFurtherObjection` | 43 | Further Objection | Nueva objeción |
| `edesResending` | 44 | Resending | Reenviando |

## Used by (2 properties)

- [EDFEntry](../Tipos-Complejos/EDFEntry.md).`Status`
- [EDFImportEntry](../Tipos-Complejos/EDFImportEntry.md).`Status`
