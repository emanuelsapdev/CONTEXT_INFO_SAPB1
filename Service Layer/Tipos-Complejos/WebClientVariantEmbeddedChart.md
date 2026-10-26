# WebClientVariantEmbeddedChart — Gráfico incrustado de la variante

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `WebClientVariantEmbeddedChart`
- **Descripción (ES):** Gráfico incrustado de la variante
- **Description (EN):** Web Client Variant Embedded Chart

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
| 10 | `WebClientVariantEmbeddedChartValue1Collection` | Collection([WebClientVariantEmbeddedChartValue1](../Tipos-Complejos/WebClientVariantEmbeddedChartValue1.md)) | Yes | Web Client Variant Embedded Chart Value 1 Collection | Colección de valores 1 del gráfico incrustado |
| 11 | `WebClientVariantEmbeddedChartValue2Collection` | Collection([WebClientVariantEmbeddedChartValue2](../Tipos-Complejos/WebClientVariantEmbeddedChartValue2.md)) | Yes | Web Client Variant Embedded Chart Value 2 Collection | Colección de valores 2 del gráfico incrustado |
| 12 | `WebClientVariantEmbeddedChartSizeCollection` | Collection([WebClientVariantEmbeddedChartSize](../Tipos-Complejos/WebClientVariantEmbeddedChartSize.md)) | Yes | Web Client Variant Embedded Chart Size Collection | Colección de tamaños de gráfico incrustado |

## Used by (properties)

- [WebClientVariant](../Entidades/WebClientVariants.md).`WebClientVariantEmbeddedChartCollection`
