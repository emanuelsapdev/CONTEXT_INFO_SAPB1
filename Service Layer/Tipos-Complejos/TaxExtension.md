# TaxExtension — Extensión de impuestos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `TaxExtension`
- **Descripción (ES):** Extensión de impuestos
- **Description (EN):** Tax Extension

- **Properties:** 57

## Properties (57)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `TaxId0` | Edm.String | Yes | Tax ID 0 | ID fiscal 0 |
| 2 | `TaxId1` | Edm.String | Yes | Tax ID 1 | ID fiscal 1 |
| 3 | `TaxId2` | Edm.String | Yes | Tax ID 2 | ID fiscal 2 |
| 4 | `TaxId3` | Edm.String | Yes | Tax ID 3 | ID fiscal 3 |
| 5 | `TaxId4` | Edm.String | Yes | Tax ID 4 | ID fiscal 4 |
| 6 | `TaxId5` | Edm.String | Yes | Tax ID 5 | ID fiscal 5 |
| 7 | `TaxId6` | Edm.String | Yes | Tax ID 6 | ID fiscal 6 |
| 8 | `TaxId7` | Edm.String | Yes | Tax ID 7 | ID fiscal 7 |
| 9 | `TaxId8` | Edm.String | Yes | Tax ID 8 | ID fiscal 8 |
| 10 | `TaxId9` | Edm.String | Yes | Tax ID 9 | ID fiscal 9 |
| 11 | `State` | Edm.String | Yes | State | Estado/provincia |
| 12 | `County` | Edm.String | Yes | County | Condado |
| 13 | `Incoterms` | Edm.String | Yes | Incoterms | Incoterms |
| 14 | `Vehicle` | Edm.String | Yes | Vehicle | Vehículo |
| 15 | `VehicleState` | Edm.String | Yes | Vehicle State | Estado del vehículo |
| 16 | `NFRef` | Edm.String | Yes | NF Ref | Referencia de NF |
| 17 | `Carrier` | Edm.String | Yes | Carrier | Transportista |
| 18 | `PackQuantity` | Edm.Int32 | Yes | Pack Quantity | Cantidad por paquete |
| 19 | `PackDescription` | Edm.String | Yes | Pack Description | Descripción del paquete |
| 20 | `Brand` | Edm.String | Yes | Brand | Marca |
| 21 | `ShipUnitNo` | Edm.Int32 | Yes | Ship Unit Number | Número de unidad de envío |
| 22 | `NetWeight` | Edm.Double | Yes | Net Weight | Peso neto |
| 23 | `GrossWeight` | Edm.Double | Yes | Gross Weight | Peso bruto |
| 24 | `StreetS` | Edm.String | Yes | Street S | Calle (envío) |
| 25 | `BlockS` | Edm.String | Yes | Block S | Barrio (envío) |
| 26 | `BuildingS` | Edm.String | Yes | Building S | Edificio (envío) |
| 27 | `CityS` | Edm.String | Yes | City S | Ciudad (envío) |
| 28 | `ZipCodeS` | Edm.String | Yes | Zip Code S | Código postal (envío) |
| 29 | `CountyS` | Edm.String | Yes | County S | Condado (envío) |
| 30 | `StateS` | Edm.String | Yes | State S | Estado/provincia (envío) |
| 31 | `CountryS` | Edm.String | Yes | Country S | País (envío) |
| 32 | `StreetB` | Edm.String | Yes | Street B | Calle (facturación) |
| 33 | `BlockB` | Edm.String | Yes | Block B | Barrio (facturación) |
| 34 | `BuildingB` | Edm.String | Yes | Building B | Edificio (facturación) |
| 35 | `CityB` | Edm.String | Yes | City B | Ciudad (facturación) |
| 36 | `ZipCodeB` | Edm.String | Yes | Zip Code B | Código postal (facturación) |
| 37 | `CountyB` | Edm.String | Yes | County B | Condado (facturación) |
| 38 | `StateB` | Edm.String | Yes | State B | Estado/provincia (facturación) |
| 39 | `CountryB` | Edm.String | Yes | Country B | País (facturación) |
| 40 | `ImportOrExport` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Import Or Export | Importación o exportación |
| 41 | `MainUsage` | Edm.Int32 | Yes | Main Usage | Uso principal |
| 42 | `GlobalLocationNumberS` | Edm.String | Yes | Global Location Number S | GLN (envío) |
| 43 | `GlobalLocationNumberB` | Edm.String | Yes | Global Location Number B | GLN (facturación) |
| 44 | `TaxId12` | Edm.String | Yes | Tax ID 12 | ID fiscal 12 |
| 45 | `TaxId13` | Edm.String | Yes | Tax ID 13 | ID fiscal 13 |
| 46 | `BillOfEntryNo` | Edm.String | Yes | Bill Of Entry Number | Número del despacho de importación |
| 47 | `BillOfEntryDate` | Edm.DateTimeOffset | Yes | Bill Of Entry Date | Fecha del despacho de importación |
| 48 | `OriginalBillOfEntryNo` | Edm.String | Yes | Original Bill Of Entry Number | Número del despacho de importación original |
| 49 | `OriginalBillOfEntryDate` | Edm.DateTimeOffset | Yes | Original Bill Of Entry Date | Fecha del despacho de importación original |
| 50 | `ImportOrExportType` | [ImportOrExportTypeEnum](../Enums/ImportOrExportTypeEnum.md) | Yes | Import Or Export Type | Tipo de importación o exportación |
| 51 | `PortCode` | Edm.String | Yes | Port Code | Código del puerto |
| 52 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 53 | `BoEValue` | Edm.Double | Yes | Bo E Value | Valor de letra de cambio |
| 54 | `ClaimRefund` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Claim Refund | Solicitar reembolso |
| 55 | `DifferentialOfTaxRate` | Edm.Int32 | Yes | Differential Of Tax Rate | Diferencial de la tasa de impuesto |
| 56 | `IsIGSTAccount` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is IGST Account | Es cuenta IGST |
| 57 | `TaxId14` | Edm.String | Yes | Tax ID 14 | ID fiscal 14 |

## Used by (properties)

- [Document](../Entidades/PurchaseQuotations.md).`TaxExtension`
