# ActivityMultipleRecipient — Destinatarios múltiples de la actividad

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ActivityMultipleRecipient`
- **Descripción (ES):** Destinatarios múltiples de la actividad
- **Description (EN):** Activity Multiple Recipient
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineNumer` | Edm.Int32 | Yes | Line Numer | Número de línea |
| 2 | `RecipientType` | [ActivityRecipientObjTypeEnum](../Enums/ActivityRecipientObjTypeEnum.md) | Yes | Recipient Type | Tipo de destinatario |
| 3 | `RecipientCode` | Edm.String | Yes | Recipient Code | Código del destinatario |

## Used by (properties)

- [Activity](../Entidades/Activities.md).`ActivityMultipleRecipients`
