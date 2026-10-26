# ProductionOrdersDocumentReference — Referencias de documentos de la orden de fabricación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ProductionOrdersDocumentReference`
- **Descripción (ES):** Referencias de documentos de la orden de fabricación
- **Description (EN):** Production Orders Document Reference
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 8

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 2 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `RefDocEntr` | Edm.Int32 | Yes | Ref Document Entr | DocEntry del documento de referencia |
| 4 | `RefDocNum` | Edm.Int32 | Yes | Ref Document Number | Número del documento de referencia |
| 5 | `ExtDocNum` | Edm.String | Yes | Ext Document Number | Número de documento externo |
| 6 | `RefObjType` | [ReferencedObjectTypeEnum](../Enums/ReferencedObjectTypeEnum.md) | Yes | Ref Obj Type | Tipo de objeto de referencia |
| 7 | `IssueDate` | Edm.DateTimeOffset | Yes | Issue Date | Fecha de emisión |
| 8 | `Remark` | Edm.String | Yes | Remark | Comentario |

## Used by (properties)

- [ProductionOrder](../Entidades/ProductionOrders.md).`ProductionOrdersDocumentReferences`
