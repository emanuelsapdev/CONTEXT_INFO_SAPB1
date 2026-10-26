# DocumentReference — Referencias del documento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DocumentReference`
- **Descripción (ES):** Referencias del documento
- **Description (EN):** Document Reference

- **Properties:** 18

## Properties (18)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 2 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `RefDocEntr` | Edm.Int32 | Yes | Ref Document Entr | DocEntry del documento de referencia |
| 4 | `RefDocNum` | Edm.Int32 | Yes | Ref Document Number | Número del documento de referencia |
| 5 | `ExtDocNum` | Edm.String | Yes | Ext Document Number | Número de documento externo |
| 6 | `RefObjType` | [ReferencedObjectTypeEnum](../Enums/ReferencedObjectTypeEnum.md) | Yes | Ref Obj Type | Tipo de objeto de referencia |
| 7 | `AccessKey` | Edm.String | Yes | Access Key | Clave de acceso |
| 8 | `IssueDate` | Edm.DateTimeOffset | Yes | Issue Date | Fecha de emisión |
| 9 | `IssuerCNPJ` | Edm.String | Yes | Issuer CNPJ | CNPJ del emisor |
| 10 | `IssuerCode` | Edm.String | Yes | Issuer Code | Código del emisor |
| 11 | `Model` | Edm.String | Yes | Model | Modelo |
| 12 | `Series` | Edm.String | Yes | Series | Serie de numeración |
| 13 | `Number` | Edm.Int32 | Yes | Number | Número |
| 14 | `RefAccKey` | Edm.String | Yes | Ref Account Key | Clave de cuenta de referencia |
| 15 | `RefAmount` | Edm.Double | Yes | Ref Amount | Importe de referencia |
| 16 | `SubSeries` | Edm.String | Yes | Sub Series | Subserie |
| 17 | `Remark` | Edm.String | Yes | Remark | Comentario |
| 18 | `LinkRefTyp` | [LinkReferenceTypeEnum](../Enums/LinkReferenceTypeEnum.md) | Yes | Link Ref Typ | Tipo de referencia de vínculo |

## Used by (properties)

- [Document](../Entidades/PurchaseQuotations.md).`DocumentReferences`
- [StockTransfer](../Entidades/StockTransfers.md).`DocumentReferences`
