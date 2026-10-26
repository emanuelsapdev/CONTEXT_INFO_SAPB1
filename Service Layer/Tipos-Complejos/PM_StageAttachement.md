# PM_StageAttachement — Anexos de etapas del proyecto

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `PM_StageAttachement`
- **Descripción (ES):** Anexos de etapas del proyecto
- **Description (EN):** PM Stage Attachement

- **Properties:** 6

## Properties (6)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` | Edm.Int32 | Yes | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `LineID` | Edm.Int32 | Yes | Line ID | ID de línea |
| 3 | `SourcePath` | Edm.String | Yes | Source Path | Ruta de origen |
| 4 | `FileName` | Edm.String | Yes | File Name | Nombre del archivo |
| 5 | `FileExtension` | Edm.String | Yes | File Extension | Extensión del archivo |
| 6 | `AttachementDate` | Edm.DateTimeOffset | Yes | Attachement Date | Fecha del anexo |

## Used by (properties)

- [PM_ProjectDocumentData](../Entidades/ProjectManagements.md).`PM_StageAttachements`
