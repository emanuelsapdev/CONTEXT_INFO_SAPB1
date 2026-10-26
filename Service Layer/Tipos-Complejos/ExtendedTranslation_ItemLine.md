# ExtendedTranslation_ItemLine — Líneas de elementos de traducción ampliada

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ExtendedTranslation_ItemLine`
- **Descripción (ES):** Líneas de elementos de traducción ampliada
- **Description (EN):** Extended Translation Item Line

- **Properties:** 9

## Properties (9)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 2 | `LineNumber` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `ItemCode` | Edm.String | Yes | Item Code | Código de artículo |
| 4 | `ItemType` | Edm.String | Yes | Item Type | Tipo de artículo |
| 5 | `SlimType` | Edm.String | Yes | Slim Type | Tipo SLIM |
| 6 | `MaxLength` | Edm.Int32 | Yes | Max Length | Longitud máxima |
| 7 | `SourceText` | Edm.String | Yes | Source Text | Texto de origen |
| 8 | `Memo` | Edm.String | Yes | Memo | Comentario |
| 9 | `ExtendedTranslation_ResultLines` | Collection([ExtendedTranslation_ResultLine](../Tipos-Complejos/ExtendedTranslation_ResultLine.md)) | Yes | Extended Translation Result Lines | Líneas de resultados de traducción ampliada |

## Used by (properties)

- [ExtendedTranslation](../Entidades/ExtendedTranslations.md).`ExtendedTranslation_ItemLines`
