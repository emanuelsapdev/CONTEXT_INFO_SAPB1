# ItemIntrastatExtension — Extensión Intrastat del artículo

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ItemIntrastatExtension`
- **Descripción (ES):** Extensión Intrastat del artículo
- **Description (EN):** Item Intrastat Extension

- **Properties:** 20

## Properties (20)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |
| 2 | `CommodityCode` | Edm.Int32 | Yes | Commodity Code | Código de mercancía |
| 3 | `SupplementaryUnit` | Edm.Int32 | Yes | Supplementary Unit | Unidad suplementaria |
| 4 | `FactorOfSupplementaryUnit` | Edm.Double | Yes | Factor Of Supplementary Unit | Factor de la unidad suplementaria |
| 5 | `ImportRegionState` | Edm.Int32 | Yes | Import Region State | Estado de la región de importación |
| 6 | `ExportRegionState` | Edm.Int32 | Yes | Export Region State | Estado de la región de exportación |
| 7 | `ImportNatureOfTransaction` | Edm.Int32 | Yes | Import Nature Of Transaction | Naturaleza de la transacción de importación |
| 8 | `ExportNatureOfTransaction` | Edm.Int32 | Yes | Export Nature Of Transaction | Naturaleza de la transacción de exportación |
| 9 | `ImportStatisticalProcedure` | Edm.Int32 | Yes | Import Statistical Procedure | Procedimiento estadístico de importación |
| 10 | `ExportStatisticalProcedure` | Edm.Int32 | Yes | Export Statistical Procedure | Procedimiento estadístico de exportación |
| 11 | `CountryOfOrigin` | Edm.String | Yes | Country Of Origin | País de origen |
| 12 | `ServiceCode` | Edm.Int32 | Yes | Service Code | Código de servicio |
| 13 | `Type` | [BoDocumentTypes](../Enums/BoDocumentTypes.md) | Yes | Type | Tipo |
| 14 | `ServiceSupplyMethod` | [BoServiceSupplyMethods](../Enums/BoServiceSupplyMethods.md) | Yes | Service Supply Method | Método de prestación de servicios |
| 15 | `ServicePaymentMethod` | [BoServicePaymentMethods](../Enums/BoServicePaymentMethods.md) | Yes | Service Payment Method | Vía de pago del servicio |
| 16 | `ImportRegionCountry` | Edm.String | Yes | Import Region Country | País de la región de importación |
| 17 | `ExportRegionCountry` | Edm.String | Yes | Export Region Country | País de la región de exportación |
| 18 | `UseWeightInCalculation` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Use Weight In Calculation | Usar peso en el cálculo |
| 19 | `IntrastatRelevant` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Intrastat Relevant | Relevante para Intrastat |
| 20 | `StatisticalCode` | Edm.String | Yes | Statistical Code | Código estadístico |

## Used by (properties)

- [Item](../Entidades/Items.md).`ItemIntrastatExtension`
