# SalesTaxInvoiceDocumentReference — Referencias de documentos de la factura de impuestos de venta

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `SalesTaxInvoiceDocumentReference`
- **Descripción (ES):** Referencias de documentos de la factura de impuestos de venta
- **Description (EN):** Sales Tax Invoice Document Reference
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 9

## Properties (9)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 2 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `ReferencedDocEntry` | Edm.Int32 | Yes | Referenced Document Entry | DocEntry del documento referenciado |
| 4 | `ReferencedDocNumber` | Edm.Int32 | Yes | Referenced Document Number | Número del documento referenciado |
| 5 | `ExternalReferencedDocNumber` | Edm.String | Yes | External Referenced Document Number | N.º de documento referenciado externo |
| 6 | `ReferencedObjectType` | [ReferencedObjectTypeEnum](../Enums/ReferencedObjectTypeEnum.md) | Yes | Referenced Object Type | Tipo de objeto referenciado |
| 7 | `IssueDate` | Edm.DateTimeOffset | Yes | Issue Date | Fecha de emisión |
| 8 | `Remark` | Edm.String | Yes | Remark | Comentario |
| 9 | `CardCode` | Edm.String | Yes | Card Code | Código del socio de negocios |

## Used by (properties)

- [SalesTaxInvoice](../Entidades/SalesTaxInvoices.md).`SalesTaxInvoiceDocumentReferences`
