# ReportLayout_TranslationLine — Líneas de traducción del formato de informe

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ReportLayout_TranslationLine`
- **Descripción (ES):** Líneas de traducción del formato de informe
- **Description (EN):** Report Layout Translation Line

- **Properties:** 8

## Properties (8)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` | Edm.String | Yes | Document Entry | DocEntry (clave interna del documento) |
| 2 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `DocName` | Edm.String | Yes | Document Name | Nombre del documento |
| 4 | `LanguageCode` | Edm.Int32 | Yes | Language Code | Código de idioma |
| 5 | `CreateDate` | Edm.DateTimeOffset | Yes | Create Date | Fecha de creación |
| 6 | `UpdateDate` | Edm.DateTimeOffset | Yes | Update Date | Fecha de actualización |
| 7 | `CreateTime` | Edm.Int32 | Yes | Create Time | Hora de creación |
| 8 | `UpdateTime` | Edm.Int32 | Yes | Update Time | Hora de actualización |

## Used by (properties)

- [ReportLayout](ReportLayout.md).`ReportLayout_TranslationLines`
