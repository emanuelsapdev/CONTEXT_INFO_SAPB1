# ImportProcess — Proceso de importación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ImportProcess`
- **Descripción (ES):** Proceso de importación
- **Description (EN):** Import Process

- **Properties:** 12

## Properties (12)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 2 | `ImportationDocumentTypeCode` | Edm.String | Yes | Importation Document Type Code | Código de tipo de documento de importación |
| 3 | `ImportationDocumentNumber` | Edm.String | Yes | Importation Document Number | Número de documento de importación |
| 4 | `DateOfRegistry_DI_DSI_DA` | Edm.DateTimeOffset | Yes | Date Of Registry DI DSI DA | Fecha de registro DI/DSI/DA |
| 5 | `CustomsClearanceDate` | Edm.DateTimeOffset | Yes | Customs Clearance Date | Fecha de despacho aduanero |
| 6 | `DrawbackRegimeConcessionAccountNumber` | Edm.String | Yes | Drawback Regime Concession Account Number | Número de cuenta de concesión del régimen drawback |
| 7 | `AdditionalNumber` | Edm.String | Yes | Additional Number | Número adicional |
| 8 | `AdditionalItemDiscountValue` | Edm.Double | Yes | Additional Item Discount Value | Valor de descuento adicional del artículo |
| 9 | `DrawbackSuspensionRegime` | Edm.String | Yes | Drawback Suspension Regime | Régimen de suspensión drawback |
| 10 | `TypeOfImport` | Edm.String | Yes | Type Of Import | Tipo de importación |
| 11 | `AdditionalFreightToNavyAuthority` | Edm.Double | Yes | Additional Freight To Navy Authority | Flete adicional a la autoridad naval |
| 12 | `AdditionalItemSequentialNumber` | Edm.Int32 | Yes | Additional Item Sequential Number | Número secuencial adicional del artículo |

## Used by (properties)

- [DocumentLine](DocumentLine.md).`ImportProcesses`
