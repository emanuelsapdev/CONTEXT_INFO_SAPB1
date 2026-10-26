# RelatedDocument — Documentos relacionados

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `RelatedDocument`
- **Descripción (ES):** Documentos relacionados
- **Description (EN):** Related Document

- **Properties:** 5

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocType` | [RelatedDocumentTypeEnum](../Enums/RelatedDocumentTypeEnum.md) | Yes | Document Type | Tipo de documento (artículos/servicios) |
| 2 | `AbsEntry` | Edm.Int32 | Yes | Abs Entry | Entrada absoluta (ID interno) |
| 3 | `UUID` | Edm.String | Yes | UUID | UUID |
| 4 | `DocTye` | [RelatedDocumentTypeEnum](../Enums/RelatedDocumentTypeEnum.md) | Yes | Document Tye | Tipo de documento |
| 5 | `AbsEnry` | Edm.Int32 | Yes | Abs Enry | Entrada absoluta (ID interno) |

## Used by (properties)

- [ElectronicProtocol](ElectronicProtocol.md).`RelatedDocuments`
