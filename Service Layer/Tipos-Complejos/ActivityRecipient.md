# ActivityRecipient — Destinatario de actividad

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ActivityRecipient`
- **Descripción (ES):** Destinatario de actividad
- **Description (EN):** Activity Recipient

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 2 | `RecipientType` | [RecipientTypeEnum](../Enums/RecipientTypeEnum.md) | Yes | Recipient Type | Tipo de destinatario |
| 3 | `RecipientCode` | Edm.String | Yes | Recipient Code | Código del destinatario |

## Used by (properties)

- [ActivityRecipientList](../Entidades/ActivityRecipientLists.md).`ActivityRecipientCollection`
