# TransportationDocumentLineData — Línea del documento de transporte

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `TransportationDocumentLineData`
- **Descripción (ES):** Línea del documento de transporte
- **Description (EN):** Transportation Document Line Data

- **Properties:** 8

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TranspDocNumber` | Edm.Int32 | Yes | Transp Document Number | Número de documento de transporte |
| 2 | `LineID` | Edm.Int32 | Yes | Line ID | ID de línea |
| 3 | `DocType` | [DocumentObjectTypeEnum](../Enums/DocumentObjectTypeEnum.md) | Yes | Document Type | Tipo de documento (artículos/servicios) |
| 4 | `DocNumber` | Edm.Int32 | Yes | Document Number | Número de documento |
| 5 | `DocLineNumber` | Edm.Int32 | Yes | Document Line Number | Número de línea del documento |
| 6 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |
| 7 | `TransportedQuantity` | Edm.Double | Yes | Transported Quantity | Cantidad transportada |
| 8 | `DocOrderNum` | Edm.Int32 | Yes | Document Order Number | Número de orden del documento |

## Used by (properties)

- [TransportationDocumentData](../Entidades/TransportationDocument.md).`TransportationDocumentLineDataCollection`
