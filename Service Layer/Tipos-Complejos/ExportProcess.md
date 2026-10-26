# ExportProcess — Proceso de exportación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ExportProcess`
- **Descripción (ES):** Proceso de exportación
- **Description (EN):** Export Process

- **Properties:** 15

## Properties (15)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 2 | `ExportationDocumentTypeCode` | Edm.Int32 | Yes | Exportation Document Type Code | Código de tipo de documento de exportación |
| 3 | `ExportationDeclarationNumber` | Edm.Int32 | Yes | Exportation Declaration Number | Número de declaración de exportación |
| 4 | `ExportationDeclarationDate` | Edm.DateTimeOffset | Yes | Exportation Declaration Date | Fecha de declaración de exportación |
| 5 | `ExportationNatureCode` | Edm.Int32 | Yes | Exportation Nature Code | Código de naturaleza de la exportación |
| 6 | `ExportationRegistryNumber` | Edm.Int32 | Yes | Exportation Registry Number | Número de registro de exportación |
| 7 | `ExportationRegistryDate` | Edm.DateTimeOffset | Yes | Exportation Registry Date | Fecha de registro de exportación |
| 8 | `LadingBillNumber` | Edm.String | Yes | Lading Bill Number | Número del conocimiento de embarque |
| 9 | `LadingBillDate` | Edm.DateTimeOffset | Yes | Lading Bill Date | Fecha del conocimiento de embarque |
| 10 | `MerchandiseLeftCustomsDate` | Edm.DateTimeOffset | Yes | Merchandise Left Customs Date | Fecha de salida de aduana de la mercancía |
| 11 | `LadingBillTypeCode` | Edm.Int32 | Yes | Lading Bill Type Code | Código de tipo de conocimiento de embarque |
| 12 | `DrawbackSuspensionRegime` | Edm.String | Yes | Drawback Suspension Regime | Régimen de suspensión drawback |
| 13 | `NatureOfExport` | Edm.String | Yes | Nature Of Export | Naturaleza de la exportación |
| 14 | `QuantityOfExportedItems` | Edm.Double | Yes | Quantity Of Exported Items | Cantidad de artículos exportados |
| 15 | `AdditionalItemSequentialNumber` | Edm.Int32 | Yes | Additional Item Sequential Number | Número secuencial adicional del artículo |

## Used by (properties)

- [DocumentLine](DocumentLine.md).`ExportProcesses`
