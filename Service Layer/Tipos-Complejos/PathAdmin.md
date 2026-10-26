# PathAdmin — Rutas de administración (carpetas)

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `PathAdmin`
- **Descripción (ES):** Rutas de administración (carpetas)
- **Description (EN):** Path Admin

- **Properties:** 5

## Properties (5)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `WordTemplateFolderPath` | Edm.String | Yes | Word Template Folder Path | Ruta de carpeta de plantillas Word |
| 2 | `PicturesFolderPath` | Edm.String | Yes | Pictures Folder Path | Ruta de carpeta de imágenes |
| 3 | `AttachmentsFolderPath` | Edm.String | Yes | Attachments Folder Path | Ruta de la carpeta de anexos |
| 4 | `ExtensionsFolderPath` | Edm.String | Yes | Extensions Folder Path | Ruta de carpeta de extensiones |
| 5 | `PrintId` | Edm.String | Yes | Print ID | ID de impresión |

## Used by (service operations)

- [`CompanyService_GetPathAdmin`](../Servicios/CompanyService.md#companyservice_getpathadmin)
- [`CompanyService_UpdatePathAdmin`](../Servicios/CompanyService.md#companyservice_updatepathadmin)
