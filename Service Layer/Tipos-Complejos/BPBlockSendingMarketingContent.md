# BPBlockSendingMarketingContent — Bloqueos de envío de contenido de marketing del socio de negocios

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `BPBlockSendingMarketingContent`
- **Descripción (ES):** Bloqueos de envío de contenido de marketing del socio de negocios
- **Description (EN):** Business Partner Block Sending Marketing Content

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `CardCode` | Edm.String | Yes | Card Code | Código del socio de negocios |
| 2 | `CommunicationMediaId` | Edm.Int32 | Yes | Communication Media ID | ID de medio de comunicación |
| 3 | `Choose` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Choose | Seleccionar |

## Used by (properties)

- [BusinessPartner](../Entidades/BusinessPartners.md).`BPBlockSendingMarketingContents`
