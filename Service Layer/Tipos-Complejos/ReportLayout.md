# ReportLayout — Formato de informe

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ReportLayout`
- **Descripción (ES):** Formato de informe
- **Description (EN):** Report Layout

- **Properties:** 48

## Properties (48)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Name` | Edm.String | Yes | Name | Nombre |
| 2 | `Author` | Edm.String | Yes | Author | Autor |
| 3 | `Remarks` | Edm.String | Yes | Remarks | Comentarios |
| 4 | `Width` | Edm.Int32 | Yes | Width | Ancho |
| 5 | `Height` | Edm.Int32 | Yes | Height | Altura |
| 6 | `LeftMargin` | Edm.Int32 | Yes | Left Margin | Margen izquierdo |
| 7 | `RightMargin` | Edm.Int32 | Yes | Right Margin | Margen derecho |
| 8 | `TopMargin` | Edm.Int32 | Yes | Top Margin | Margen superior |
| 9 | `BottomMargin` | Edm.Int32 | Yes | Bottom Margin | Margen inferior |
| 10 | `Editable` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Editable | Editable |
| 11 | `PaperSize` | Edm.String | Yes | Paper Size | Tamaño de papel |
| 12 | `Orientation` | [BoOrientationEnum](../Enums/BoOrientationEnum.md) | Yes | Orientation | Orientación |
| 13 | `GridSize` | Edm.Int32 | Yes | Grid Size | Tamaño de cuadrícula |
| 14 | `GridType` | [BoGridTypeEnum](../Enums/BoGridTypeEnum.md) | Yes | Grid Type | Tipo de cuadrícula |
| 15 | `ShowGrid` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Show Grid | Mostrar cuadrícula |
| 16 | `SnapToGrid` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Snap To Grid | Ajustar a la cuadrícula |
| 17 | `Picture` | Edm.String | Yes | Picture | Imagen |
| 18 | `TypeCode` | Edm.String | Yes | Type Code | Código de tipo |
| 19 | `ForeignLanguageReport` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Foreign Language Report | Informe en idioma extranjero |
| 20 | `Sortable` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Sortable | Ordenable |
| 21 | `LeaderReport` | Edm.String | Yes | Leader Report | Informe principal |
| 22 | `FollowUpReport` | Edm.String | Yes | Follow Up Report | Informe de seguimiento |
| 23 | `ConvertFontInPrintPreview` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Convert Font In Print Preview | Convertir fuente en vista previa de impresión |
| 24 | `PreviewPrintingFont` | Edm.String | Yes | Preview Printing Font | Fuente de vista previa de impresión |
| 25 | `ChangeFontSizeInPreview` | Edm.Int32 | Yes | Change Font Size In Preview | Cambiar tamaño de fuente en vista previa |
| 26 | `ConvertFontForEMail` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Convert Font For E Mail | Convertir fuente para correo electrónico |
| 27 | `EMailFont` | Edm.String | Yes | E Mail Font | Fuente de correo electrónico |
| 28 | `ChangeFontSizeForEMail` | Edm.Int32 | Yes | Change Font Size For E Mail | Cambiar tamaño de fuente para correo electrónico |
| 29 | `Query` | Edm.String | Yes | Query | Consulta |
| 30 | `QueryType` | [BoQueryTypeEnum](../Enums/BoQueryTypeEnum.md) | Yes | Query Type | Tipo de consulta |
| 31 | `language` | Edm.Int32 | Yes | Language | Idioma |
| 32 | `ImpExpObjCode` | Edm.Int32 | Yes | Imp Exp Obj Code | Código de objeto de importación/exportación |
| 33 | `ExtensionName` | Edm.String | Yes | Extension Name | Nombre de la extensión |
| 34 | `ExtensionErrorAction` | [BoExtensionErrorActionEnum](../Enums/BoExtensionErrorActionEnum.md) | Yes | Extension Error Action | Acción ante error de extensión |
| 35 | `RepetitiveAreasNumber` | Edm.Int32 | Yes | Repetitive Areas Number | Cantidad de áreas repetitivas |
| 36 | `AllignFooterToBottom` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Allign Footer To Bottom | Alinear pie de página abajo |
| 37 | `LayoutCode` | Edm.String | Yes | Layout Code | Código de formato |
| 38 | `Category` | [ReportLayoutCategoryEnum](../Enums/ReportLayoutCategoryEnum.md) | Yes | Category | Categoría |
| 39 | `Printer` | Edm.String | Yes | Printer | Impresora |
| 40 | `PrinterFirstPage` | Edm.String | Yes | Printer First Page | Primera página en impresora |
| 41 | `NumberOfCopies` | Edm.Int32 | Yes | Number Of Copies | Cantidad de copias |
| 42 | `Localization` | Edm.String | Yes | Localization | Localización |
| 43 | `UseFirstPrinter` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Use First Printer | Usar la primera impresora |
| 44 | `B1Version` | Edm.String | Yes | B 1 Version | Versión de SAP Business One |
| 45 | `CRVersion` | Edm.String | Yes | CR Version | Versión de Crystal Reports |
| 46 | `TypeDetail` | Edm.String | Yes | Type Detail | Detalle del tipo |
| 47 | `ReportLayoutItems` | Collection([ReportLayoutItem](../Tipos-Complejos/ReportLayoutItem.md)) | Yes | Report Layout Items | Elementos del formato de informe |
| 48 | `ReportLayout_TranslationLines` | Collection([ReportLayout_TranslationLine](../Tipos-Complejos/ReportLayout_TranslationLine.md)) | Yes | Report Layout Translation Lines | Líneas de traducción del formato de informe |

## Used by (service operations)

- [`ReportLayoutsService_AddReportLayout`](../Servicios/ReportLayoutsService.md#reportlayoutsservice_addreportlayout)
- [`ReportLayoutsService_AddReportLayoutToMenu`](../Servicios/ReportLayoutsService.md#reportlayoutsservice_addreportlayouttomenu)
- [`ReportLayoutsService_GetDefaultReportLayout`](../Servicios/ReportLayoutsService.md#reportlayoutsservice_getdefaultreportlayout)
- [`ReportLayoutsService_GetReportLayout`](../Servicios/ReportLayoutsService.md#reportlayoutsservice_getreportlayout)
- [`ReportLayoutsService_UpdateLanguageReport`](../Servicios/ReportLayoutsService.md#reportlayoutsservice_updatelanguagereport)
- [`ReportLayoutsService_UpdatePrinterSettings`](../Servicios/ReportLayoutsService.md#reportlayoutsservice_updateprintersettings)
