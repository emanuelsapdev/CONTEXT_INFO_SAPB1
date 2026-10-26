# AlertManagementRecipient — Destinatarios de la gestión de alertas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `AlertManagementRecipient`
- **Descripción (ES):** Destinatarios de la gestión de alertas
- **Description (EN):** Alert Management Recipient

- **Properties:** 5

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `UserCode` | Edm.Int32 | Yes | User Code | Código de usuario |
| 2 | `SendEMail` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Send E Mail | Enviar correo electrónico |
| 3 | `SendSMS` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Send SMS | Enviar SMS |
| 4 | `SendFax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Send Fax | Enviar fax |
| 5 | `SendInternal` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Send Internal | Enviar interno |

## Used by (properties)

- [AlertManagement](../Entidades/AlertManagements.md).`AlertManagementRecipients`
