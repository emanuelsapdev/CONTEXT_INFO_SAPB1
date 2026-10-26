# Recipient — Destinatario

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `Recipient`
- **Descripción (ES):** Destinatario
- **Description (EN):** Recipient

- **Properties:** 10

## Properties (10)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `UserCode` | Edm.String | Yes | User Code | Código de usuario |
| 2 | `UserType` | [BoMsgRcpTypes](../Enums/BoMsgRcpTypes.md) | Yes | User Type | Tipo de usuario |
| 3 | `NameTo` | Edm.String | Yes | Name To | Nombre hasta |
| 4 | `SendEmail` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Send Email | Enviar correo electrónico |
| 5 | `EmailAddress` | Edm.String | Yes | Email Address | Dirección de correo electrónico |
| 6 | `SendSMS` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Send SMS | Enviar SMS |
| 7 | `CellularNumber` | Edm.String | Yes | Cellular Number | Número de celular |
| 8 | `SendFax` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Send Fax | Enviar fax |
| 9 | `FaxNumber` | Edm.String | Yes | Fax Number | Número de fax |
| 10 | `SendInternal` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Send Internal | Enviar interno |

## Used by (properties)

- [Message](../Entidades/Messages.md).`RecipientCollection`
