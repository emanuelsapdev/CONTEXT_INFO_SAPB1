# BOEDocumentTypeParams — Parámetros de tipos de documento de letras de cambio

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `BOEDocumentTypeParams`
- **Descripción (ES):** Parámetros de tipos de documento de letras de cambio
- **Description (EN):** BOE Document Type Parameters

- **Properties:** 2

## Properties (2)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `DocEntry` | Edm.Int32 | Yes | Document Entry | DocEntry (clave interna del documento) |
| 2 | `DocType` | Edm.String | Yes | Document Type | Tipo de documento (artículos/servicios) |

## Used by (service operations)

- [`BOEDocumentTypesService_GetBOEDocumentTypeList`](../Servicios/BOEDocumentTypesService.md#boedocumenttypesservice_getboedocumenttypelist)
