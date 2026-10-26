# Attachments2_Line — Líneas de anexos

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `Attachments2_Line`
- **Descripción (ES):** Líneas de anexos
- **Description (EN):** Attachments 2 Line
- **Open type:** yes (may carry dynamic properties)
- **Properties:** 18

## Properties (18)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsoluteEntry` | Edm.Int32 | Yes | Absolute Entry | Entrada absoluta (ID interno) |
| 2 | `LineNum` | Edm.Int32 | Yes | Line Number | Número de línea |
| 3 | `SourcePath` | Edm.String | Yes | Source Path | Ruta de origen |
| 4 | `FileName` | Edm.String | Yes | File Name | Nombre del archivo |
| 5 | `FileExtension` | Edm.String | Yes | File Extension | Extensión del archivo |
| 6 | `AttachmentDate` | Edm.DateTimeOffset | Yes | Attachment Date | Fecha del anexo |
| 7 | `UserID` | Edm.Int32 | Yes | User ID | ID de usuario |
| 8 | `Override` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Override | Sobrescribir |
| 9 | `FreeText` | Edm.String | Yes | Free Text | Texto libre |
| 10 | `CopyToTargetDoc` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Copy To Target Document | Copiar al documento destino |
| 11 | `CopyToProductionOrder` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Copy To Production Order | Copiar a orden de fabricación |
| 12 | `EDocSign` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | E Document Sign | Firma del documento electrónico |
| 13 | `TargetPath` | Edm.String | Yes | Target Path | Ruta de destino |
| 14 | `SubPath` | Edm.String | Yes | Sub Path | Subruta |
| 15 | `SendInMail` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Send In Mail | Enviar por correo |
| 16 | `FileSize` | Edm.Int32 | Yes | File Size | Tamaño del archivo |
| 17 | `CopyFile` | Edm.String | Yes | Copy File | Copiar archivo |
| 18 | `FileSuffix` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | File Suffix | Sufijo del archivo |

## Used by (properties)

- [Attachments2](../Entidades/Attachments2.md).`Attachments2_Lines`
