# WebClientVariantMChart — Gráfico M de la variante

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `WebClientVariantMChart`
- **Descripción (ES):** Gráfico M de la variante
- **Description (EN):** Web Client Variant M Chart

- **Properties:** 12

## Properties (12)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Guid` | Edm.String | Yes | Guid | GUID |
| 2 | `ChartType` | Edm.String | Yes | Chart Type | Tipo de gráfico |
| 3 | `IsShowLegend` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Show Legend | Mostrar leyenda |
| 4 | `CategoryAxis1` | Edm.String | Yes | Category Axis 1 | Eje de categoría 1 |
| 5 | `CategoryAxis2` | Edm.String | Yes | Category Axis 2 | Eje de categoría 2 |
| 6 | `TimeAxis` | Edm.String | Yes | Time Axis | Eje de tiempo |
| 7 | `Color` | Edm.String | Yes | Color | Color |
| 8 | `Shape` | Edm.String | Yes | Shape | Forma |
| 9 | `BubbleWidth` | Edm.String | Yes | Bubble Width | Ancho de burbuja |
| 10 | `WebClientVariantMChartValue1Collection` | Collection([WebClientVariantMChartValue1](../Tipos-Complejos/WebClientVariantMChartValue1.md)) | Yes | Web Client Variant M Chart Value 1 Collection | Colección de valores 1 del gráfico M |
| 11 | `WebClientVariantMChartValue2Collection` | Collection([WebClientVariantMChartValue2](../Tipos-Complejos/WebClientVariantMChartValue2.md)) | Yes | Web Client Variant M Chart Value 2 Collection | Colección de valores 2 del gráfico M |
| 12 | `WebClientVariantMChartSizeCollection` | Collection([WebClientVariantMChartSize](../Tipos-Complejos/WebClientVariantMChartSize.md)) | Yes | Web Client Variant M Chart Size Collection | Colección de tamaños de gráfico M |

## Used by (properties)

- [WebClientVariant](../Entidades/WebClientVariants.md).`WebClientVariantMChartCollection`
