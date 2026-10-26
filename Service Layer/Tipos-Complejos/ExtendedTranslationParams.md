# ExtendedTranslationParams — Parámetros de traducciones ampliadas

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `ExtendedTranslationParams`
- **Descripción (ES):** Parámetros de traducciones ampliadas
- **Description (EN):** Extended Translation Parameters

- **Properties:** 4

## Properties (4)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 2 | `Category` | [TranslationCategoryEnum](../Enums/TranslationCategoryEnum.md) | Yes | Category | Categoría |
| 3 | `ID` | Edm.String | Yes | ID | ID |
| 4 | `SecondaryID` | Edm.String | Yes | Secondary ID | ID secundario |

## Used by (service operations)

- [`ExtendedTranslationsService_GetExtendedTranslationList`](../Servicios/ExtendedTranslationsService.md#extendedtranslationsservice_getextendedtranslationlist)
