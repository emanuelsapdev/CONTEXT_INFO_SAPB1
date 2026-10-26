# ContactEmployeeBlockSendingMarketingContent — Bloqueos de envío de marketing de la persona de contacto

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ContactEmployeeBlockSendingMarketingContent`
- **Descripción (ES):** Bloqueos de envío de marketing de la persona de contacto
- **Description (EN):** Contact Employee Block Sending Marketing Content

- **Properties:** 5

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ContactEmployeeAbsEntry` | Edm.Int32 | Yes | Contact Employee Abs Entry | Entrada de persona de contacto |
| 2 | `CommunicationMediaId` | Edm.Int32 | Yes | Communication Media ID | ID de medio de comunicación |
| 3 | `Choose` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Choose | Seleccionar |
| 4 | `CardCode` | Edm.String | Yes | Card Code | Código del socio de negocios |
| 5 | `ContactPersonName` | Edm.String | Yes | Contact Person Name | Nombre de persona de contacto |

## Used by (properties)

- [ContactEmployee](ContactEmployee.md).`ContactEmployeeBlockSendingMarketingContents`
