# DocumentChangeMenuName — Cambio de nombre de menú de documento

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `DocumentChangeMenuName`
- **Descripción (ES):** Cambio de nombre de menú de documento
- **Description (EN):** Document Change Menu Name

- **Properties:** 3

## Properties (3)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `Document` | Edm.String | Yes | Document | Documento |
| 2 | `DocumentSubType` | Edm.String | Yes | Document Sub Type | Subtipo de documento |
| 3 | `ChangedMenuName` | Edm.String | Yes | Changed Menu Name | Nombre de menú modificado |

## Used by (service operations)

- [`SeriesService_ChangeDocumentMenuName`](../Servicios/SeriesService.md#seriesservice_changedocumentmenuname)
- [`SeriesService_GetDocumentChangedMenuName`](../Servicios/SeriesService.md#seriesservice_getdocumentchangedmenuname)
