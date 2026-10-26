# MailParam — Parámetros de correo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `MailParam`
- **Descripción (ES):** Parámetros de correo
- **Description (EN):** Mail Parameter

- **Properties:** 5

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Subject` | Edm.String | Yes | Subject | Asunto |
| 2 | `Body` | Edm.String | Yes | Body | Cuerpo |
| 3 | `SenderUserId` | Edm.Int32 | Yes | Sender User ID | ID de usuario remitente |
| 4 | `AttachmentId` | Edm.Int32 | Yes | Attachment ID | ID de anexo |
| 5 | `EmailRecipients` | Collection([EmailRecipient](../Tipos-Complejos/EmailRecipient.md)) | Yes | Email Recipients | Destinatarios de correo |
