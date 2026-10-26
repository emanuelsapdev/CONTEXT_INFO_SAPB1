# LandedCost_ItemLine — Líneas de artículos del costo de importación

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `LandedCost_ItemLine`
- **Descripción (ES):** Líneas de artículos del costo de importación
- **Description (EN):** Landed Cost Item Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 79

## Properties (79)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 2 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `BaseDocumentType` | [LandedCostBaseDocumentTypeEnum](../Enums/LandedCostBaseDocumentTypeEnum.md) | Yes | Base Document Type | Tipo de documento base |
| 4 | `BaseEntry` | Edm.Int32 | Yes | Base Entry | Entrada base (DocEntry del documento base) |
| 5 | `Number` | Edm.String | Yes | Number | Número |
| 6 | `ItemDescription` | Edm.String | Yes | Item Description | Descripción del artículo |
| 7 | `Quantity` | Edm.Double | Yes | Quantity | Cantidad |
| 8 | `BaseDocumentPrice` | Edm.Double | Yes | Base Document Price | Precio del documento base |
| 9 | `Rate` | Edm.Double | Yes | Rate | Tasa / tipo de cambio |
| 10 | `ProjectedCustoms` | Edm.Double | Yes | Projected Customs | Aduana proyectada |
| 11 | `ProjectedCustomsFC` | Edm.Double | Yes | Projected Customs FC (foreign currency) | Aduana proyectada (ME) |
| 12 | `Expenditure` | Edm.Double | Yes | Expenditure | Gasto |
| 13 | `ExpenditureFC` | Edm.Double | Yes | Expenditure FC (foreign currency) | Gasto (ME) |
| 14 | `WarehousePrice` | Edm.Double | Yes | Warehouse Price | Precio de almacén |
| 15 | `WarehousePriceFC` | Edm.Double | Yes | Warehouse Price FC (foreign currency) | Precio de almacén (ME) |
| 16 | `LineTotal` | Edm.Double | Yes | Line Total | Total de línea |
| 17 | `LineTotalFC` | Edm.Double | Yes | Line Total FC (foreign currency) | Total de línea (ME) |
| 18 | `Volume` | Edm.Double | Yes | Volume | Volumen |
| 19 | `VolumeUoM` | Edm.Int32 | Yes | Volume Uo M | Unidad de medida de volumen |
| 20 | `Weight1` | Edm.Double | Yes | Weight 1 | Peso 1 |
| 21 | `Weight1UnitCode` | Edm.Int32 | Yes | Weight 1 Unit Code | Código de unidad de peso 1 |
| 22 | `Weight2` | Edm.Double | Yes | Weight 2 | Peso 2 |
| 23 | `Weight2UnitCode` | Edm.Int32 | Yes | Weight 2 Unit Code | Código de unidad de peso 2 |
| 24 | `VendorCode` | Edm.String | Yes | Vendor Code | Código de proveedor |
| 25 | `Reference` | Edm.String | Yes | Reference | Referencia |
| 26 | `FactorWithoutCustoms` | Edm.Double | Yes | Factor Without Customs | Factor sin aduana |
| 27 | `FactorWithCustoms` | Edm.Double | Yes | Factor With Customs | Factor con aduana |
| 28 | `InventoryUoM` | Edm.String | Yes | Inventory Uo M | Unidad de medida de inventario |
| 29 | `BlockNumber` | Edm.String | Yes | Block Number | Número de bloque |
| 30 | `ImportLog` | Edm.String | Yes | Import Log | Registro de importación |
| 31 | `OriginalWarehouse` | Edm.String | Yes | Original Warehouse | Almacén original |
| 32 | `Warehouse` | Edm.String | Yes | Warehouse | Almacén |
| 33 | `ReleaseNumber` | Edm.Int32 | Yes | Release Number | Número de liberación |
| 34 | `VariantCosts` | Edm.Double | Yes | Variant Costs | Costos variables |
| 35 | `FixCosts` | Edm.Double | Yes | Fix Costs | Costos fijos |
| 36 | `VariantCostsFC` | Edm.Double | Yes | Variant Costs FC (foreign currency) | Costos variables (ME) |
| 37 | `FixCostsFC` | Edm.Double | Yes | Fix Costs FC (foreign currency) | Costos fijos (ME) |
| 38 | `Customs` | Edm.Double | Yes | Customs | Aduana |
| 39 | `CustomsFC` | Edm.Double | Yes | Customs FC (foreign currency) | Aduana (ME) |
| 40 | `BaseDocumentValueLineTotal` | Edm.Double | Yes | Base Document Value Line Total | Total de línea del documento base |
| 41 | `BaseDocumentValueLineTotalFC` | Edm.Double | Yes | Base Document Value Line Total FC (foreign currency) | Total de línea del documento base (ME) |
| 42 | `AllocatedUnitCostsLineTotal` | Edm.Double | Yes | Allocated Unit Costs Line Total | Total de línea de costos unitarios asignados |
| 43 | `AllocatedUnitCostsLineTotalFC` | Edm.Double | Yes | Allocated Unit Costs Line Total FC (foreign currency) | Total de línea de costos unitarios asignados (ME) |
| 44 | `CustomsValue` | Edm.Double | Yes | Customs Value | Valor en aduana |
| 45 | `CustomsValueFC` | Edm.Double | Yes | Customs Value FC (foreign currency) | Valor en aduana (ME) |
| 46 | `TotalCosts` | Edm.Double | Yes | Total Costs | Costos totales |
| 47 | `TotalCostsFC` | Edm.Double | Yes | Total Costs FC (foreign currency) | Costos totales (ME) |
| 48 | `TotalVolume` | Edm.Double | Yes | Total Volume | Volumen total |
| 49 | `BaseLine` | Edm.Int32 | Yes | Base Line | Línea base (LineNum del documento base) |
| 50 | `TotalLineProjectedCustoms` | Edm.Double | Yes | Total Line Projected Customs | Total de línea de aduana proyectada |
| 51 | `AllocatedCostsLineTotal` | Edm.Double | Yes | Allocated Costs Line Total | Total de línea de costos asignados |
| 52 | `FOBandIncludedCosts` | Edm.Double | Yes | FO Band Included Costs | FOB y costos incluidos |
| 53 | `FOBandIncludedCostsFC` | Edm.Double | Yes | FO Band Included Costs FC (foreign currency) | FOB y costos incluidos (ME) |
| 54 | `Project` | Edm.String | Yes | Project | Proyecto |
| 55 | `DistributionRule` | Edm.String | Yes | Distribution Rule | Norma de reparto |
| 56 | `DistributionRule2` | Edm.String | Yes | Distribution Rule 2 | Norma de reparto 2 |
| 57 | `DistributionRule3` | Edm.String | Yes | Distribution Rule 3 | Norma de reparto 3 |
| 58 | `DistributionRule4` | Edm.String | Yes | Distribution Rule 4 | Norma de reparto 4 |
| 59 | `DistributionRule5` | Edm.String | Yes | Distribution Rule 5 | Norma de reparto 5 |
| 60 | `PriceList` | Edm.Int32 | Yes | Price List | Lista de precios |
| 61 | `AutomaticExpenditure` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Automatic Expenditure | Gasto automático |
| 62 | `InventoryValuation` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Inventory Valuation | Valoración de inventario |
| 63 | `OriginLine` | Edm.Int32 | Yes | Origin Line | Línea de origen |
| 64 | `Currency` | Edm.String | Yes | Currency | Moneda |
| 65 | `CustomsGroupRate` | Edm.Double | Yes | Customs Group Rate | Tasa del grupo aduanero |
| 66 | `VatGroup` | Edm.String | Yes | Vat Group | Grupo de IVA (indicador de impuesto) |
| 67 | `VatPercent` | Edm.Double | Yes | Vat Percent | Porcentaje de IVA |
| 68 | `ExciseSum` | Edm.Double | Yes | Excise Sum | Importe de impuestos especiales |
| 69 | `ExciseSumFC` | Edm.Double | Yes | Excise Sum FC (foreign currency) | Importe de impuestos especiales (ME) |
| 70 | `ExciseAffectStock` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Excise Affect Stock | Impuestos especiales afectan el stock |
| 71 | `CustomsCost` | Edm.Double | Yes | Customs Cost | Costo de aduana |
| 72 | `CustomsCostFC` | Edm.Double | Yes | Customs Cost FC (foreign currency) | Costo de aduana (ME) |
| 73 | `CustomsAffectStock` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Customs Affect Stock | Aduana afecta el stock |
| 74 | `CustomsVat` | Edm.Double | Yes | Customs Vat | IVA de aduana |
| 75 | `CustomsVatFC` | Edm.Double | Yes | Customs Vat FC (foreign currency) | IVA de aduana (ME) |
| 76 | `CustomsVatAffectStock` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Customs Vat Affect Stock | IVA de aduana afecta el stock |
| 77 | `CCDNumber` | Edm.String | Yes | CCD Number | Número de declaración aduanera de carga |
| 78 | `CorrectedBaseDocumentValue` | Edm.Double | Yes | Corrected Base Document Value | Valor corregido del documento base |
| 79 | `CorrectedBaseDocumentValueFC` | Edm.Double | Yes | Corrected Base Document Value FC (foreign currency) | Valor corregido del documento base (ME) |

## Used by (properties)

- [LandedCost](../Entidades/LandedCosts.md).`LandedCost_ItemLines`
