# RecurringPostingsDocumentReference — Referencia de documento de contabilización periódica

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `RecurringPostingsDocumentReference`
- **Descripción (ES):** Referencia de documento de contabilización periódica
- **Description (EN):** Recurring Postings Document Reference

- **Properties:** 8

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `RcrCode` | Edm.String | Yes | Rcr Code | Código de recurrencia |
| 2 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `ReferencedDocEntry` | Edm.Int32 | Yes | Referenced Document Entry | DocEntry del documento referenciado |
| 4 | `ReferencedDocNumber` | Edm.Int32 | Yes | Referenced Document Number | Número del documento referenciado |
| 5 | `ExternalReferencedDocNumber` | Edm.String | Yes | External Referenced Document Number | N.º de documento referenciado externo |
| 6 | `ReferencedObjectType` | [ReferencedObjectTypeEnum](../Enums/ReferencedObjectTypeEnum.md) | Yes | Referenced Object Type | Tipo de objeto referenciado |
| 7 | `IssueDate` | Edm.DateTimeOffset | Yes | Issue Date | Fecha de emisión |
| 8 | `Remark` | Edm.String | Yes | Remark | Comentario |

## Used by (properties)

- [RecurringPostings](../Entidades/RecurringPostings.md).`RecurringPostingsDocumentReferenceCollection`
