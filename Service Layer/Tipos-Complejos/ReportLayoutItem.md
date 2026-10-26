# ReportLayoutItem — Elementos del formato de informe

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ReportLayoutItem`
- **Descripción (ES):** Elementos del formato de informe
- **Description (EN):** Report Layout Item

- **Properties:** 69

## Properties (69)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `FieldIdentifier` | Edm.String | Yes | Field Identifier | Identificador del campo |
| 2 | `ParentType` | Edm.Int32 | Yes | Parent Type | Tipo de padre |
| 3 | `Type` | [BoReportLayoutItemTypeEnum](../Enums/BoReportLayoutItemTypeEnum.md) | Yes | Type | Tipo |
| 4 | `Visible` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Visible | Visible |
| 5 | `SuppressZeros` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Suppress Zeros | Suprimir ceros |
| 6 | `Left` | Edm.Int32 | Yes | Left | Izquierda |
| 7 | `Top` | Edm.Int32 | Yes | Top | Superior |
| 8 | `Width` | Edm.Int32 | Yes | Width | Ancho |
| 9 | `Height` | Edm.Int32 | Yes | Height | Altura |
| 10 | `LeftMargin` | Edm.Int32 | Yes | Left Margin | Margen izquierdo |
| 11 | `RightMargin` | Edm.Int32 | Yes | Right Margin | Margen derecho |
| 12 | `TopMargin` | Edm.Int32 | Yes | Top Margin | Margen superior |
| 13 | `BottomMargin` | Edm.Int32 | Yes | Bottom Margin | Margen inferior |
| 14 | `LeftBorderLineThickness` | Edm.Int32 | Yes | Left Border Line Thickness | Grosor de línea del borde izquierdo |
| 15 | `RightBorderLineThickness` | Edm.Int32 | Yes | Right Border Line Thickness | Grosor de línea del borde derecho |
| 16 | `TopBorderLineThickness` | Edm.Int32 | Yes | Top Border Line Thickness | Grosor de línea del borde superior |
| 17 | `BottomBorderLineThickness` | Edm.Int32 | Yes | Bottom Border Line Thickness | Grosor de línea del borde inferior |
| 18 | `ShadowThickness` | Edm.Int32 | Yes | Shadow Thickness | Grosor de sombra |
| 19 | `BackgroundRed` | Edm.Int32 | Yes | Background Red | Color de fondo (rojo) |
| 20 | `BackgroundGreen` | Edm.Int32 | Yes | Background Green | Color de fondo (verde) |
| 21 | `BackgroundBlue` | Edm.Int32 | Yes | Background Blue | Color de fondo (azul) |
| 22 | `TextRed` | Edm.Int32 | Yes | Text Red | Color de texto (rojo) |
| 23 | `TextGreen` | Edm.Int32 | Yes | Text Green | Color de texto (verde) |
| 24 | `TextBlue` | Edm.Int32 | Yes | Text Blue | Color de texto (azul) |
| 25 | `HighlightRed` | Edm.Int32 | Yes | Highlight Red | Color de resaltado (rojo) |
| 26 | `HighlightGreen` | Edm.Int32 | Yes | Highlight Green | Color de resaltado (verde) |
| 27 | `HighlightBlue` | Edm.Int32 | Yes | Highlight Blue | Color de resaltado (azul) |
| 28 | `BorderRed` | Edm.Int32 | Yes | Border Red | Color de borde (rojo) |
| 29 | `BorderGreen` | Edm.Int32 | Yes | Border Green | Color de borde (verde) |
| 30 | `BorderBlue` | Edm.Int32 | Yes | Border Blue | Color de borde (azul) |
| 31 | `GroupNumber` | Edm.Int32 | Yes | Group Number | Número de grupo |
| 32 | `FontName` | Edm.String | Yes | Font Name | Nombre de fuente |
| 33 | `FontSize` | Edm.Int32 | Yes | Font Size | Tamaño de fuente |
| 34 | `TextStyle` | Edm.Int32 | Yes | Text Style | Estilo de texto |
| 35 | `HorizontalAlignment` | [BoHorizontalAlignmentEnum](../Enums/BoHorizontalAlignmentEnum.md) | Yes | Horizontal Alignment | Alineación horizontal |
| 36 | `LineBreak` | [BoLineBreakEnum](../Enums/BoLineBreakEnum.md) | Yes | Line Break | Salto de línea |
| 37 | `PictureSize` | [BoPictureSizeEnum](../Enums/BoPictureSizeEnum.md) | Yes | Picture Size | Tamaño de la imagen |
| 38 | `DataSource` | [BoDataSourceEnum](../Enums/BoDataSourceEnum.md) | Yes | Data Source | Origen de datos |
| 39 | `String` | Edm.String | Yes | String | Cadena |
| 40 | `VariableNumber` | Edm.Int32 | Yes | Variable Number | Número variable |
| 41 | `TableName` | Edm.String | Yes | Table Name | Nombre de la tabla |
| 42 | `FieldName` | Edm.String | Yes | Field Name | Nombre del campo |
| 43 | `DisplayDescription` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Display Description | Mostrar descripción |
| 44 | `Editable` | Edm.Int32 | Yes | Editable | Editable |
| 45 | `ItemNumber` | Edm.Int32 | Yes | Item Number | Número de artículo |
| 46 | `VerticalAlignment` | [BoVerticalAlignmentEnum](../Enums/BoVerticalAlignmentEnum.md) | Yes | Vertical Alignment | Alineación vertical |
| 47 | `SortLevel` | Edm.Int32 | Yes | Sort Level | Nivel de orden |
| 48 | `ReverseSort` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Reverse Sort | Orden inverso |
| 49 | `SortType` | [BoSortTypeEnum](../Enums/BoSortTypeEnum.md) | Yes | Sort Type | Tipo de orden |
| 50 | `Unique` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Unique | Único |
| 51 | `SetAsGroup` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Set As Group | Establecer como grupo |
| 52 | `NewPage` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | New Page | Nueva página |
| 53 | `PrintAsBarCode` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Print As Bar Code | Imprimir como código de barras |
| 54 | `LinkToField` | Edm.String | Yes | Link To Field | Vincular a campo |
| 55 | `BarCodeStandard` | [BoBarCodeStandardEnum](../Enums/BoBarCodeStandardEnum.md) | Yes | Bar Code Standard | Estándar de código de barras |
| 56 | `DisplayTotalAsAWord` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Display Total As A Word | Mostrar total en letras |
| 57 | `BlockFontChange` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Block Font Change | Bloquear cambio de fuente |
| 58 | `ParentIndex` | Edm.Int32 | Yes | Parent Index | Índice del padre |
| 59 | `ItemIndex` | Edm.Int32 | Yes | Item Index | Índice del artículo |
| 60 | `StringLength` | Edm.Int32 | Yes | String Length | Longitud de cadena |
| 61 | `StringFiller` | Edm.String | Yes | String Filler | Relleno de cadena |
| 62 | `RelateToField` | Edm.String | Yes | Relate To Field | Relacionar con campo |
| 63 | `NextSegmentItemNumber` | Edm.String | Yes | Next Segment Item Number | Siguiente número de artículo del segmento |
| 64 | `HeightAdjustments` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Height Adjustments | Ajustes de altura |
| 65 | `DuplicateRepetitiveArea` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Duplicate Repetitive Area | Duplicar área repetitiva |
| 66 | `NumberOfLinesInRepetitiveArea` | Edm.Int32 | Yes | Number Of Lines In Repetitive Area | Cantidad de líneas en el área repetitiva |
| 67 | `DistanceToRepetitiveDuplicate` | Edm.Int32 | Yes | Distance To Repetitive Duplicate | Distancia al duplicado repetitivo |
| 68 | `HideRepetitiveAreaIfEmpty` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Hide Repetitive Area If Empty | Ocultar área repetitiva si está vacía |
| 69 | `DisplayRepetitiveAreaFooterOnAllPages` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Display Repetitive Area Footer On All Pages | Mostrar pie del área repetitiva en todas las páginas |

## Used by (properties)

- [ReportLayout](ReportLayout.md).`ReportLayoutItems`
