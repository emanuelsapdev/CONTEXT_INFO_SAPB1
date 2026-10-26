# BlanketAgreementsDocument — Documento del acuerdo global

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `BlanketAgreementsDocument`
- **Descripción (ES):** Documento del acuerdo global
- **Description (EN):** Blanket Agreements Document

- **Properties:** 15

## Properties (15)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AgreementRowNumber` | Edm.Int32 | Yes | Agreement Row Number | Número de línea del acuerdo |
| 2 | `DocumentType` | [BlanketAgreementDocTypeEnum](../Enums/BlanketAgreementDocTypeEnum.md) | Yes | Document Type | Tipo de documento |
| 3 | `DocumentNo` | Edm.Int32 | Yes | Document Number | Número de documento |
| 4 | `DocumentRowNumber` | Edm.Int32 | Yes | Document Row Number | Número de línea del documento |
| 5 | `DocumentDate` | Edm.DateTimeOffset | Yes | Document Date | Fecha del documento |
| 6 | `ItemNo` | Edm.String | Yes | Item Number | Número de artículo |
| 7 | `ItemDescription` | Edm.String | Yes | Item Description | Descripción del artículo |
| 8 | `UnitPrice` | Edm.Double | Yes | Unit Price | Precio unitario |
| 9 | `Quantity` | Edm.Double | Yes | Quantity | Cantidad |
| 10 | `Discount` | Edm.Double | Yes | Discount | Descuento |
| 11 | `UoM` | Edm.String | Yes | Uo M | Unidad de medida |
| 12 | `RowStatus` | [BoStatus](../Enums/BoStatus.md) | Yes | Row Status | Estado de línea |
| 13 | `UoMCode` | Edm.String | Yes | Uo M Code | Código de unidad de medida |
| 14 | `UnitsOfMeasurement` | Edm.Double | Yes | Units Of Measurement | Unidades de medida |
| 15 | `DocStatus` | [BADocumentStatus](../Enums/BADocumentStatus.md) | Yes | Document Status | Estado del documento |
