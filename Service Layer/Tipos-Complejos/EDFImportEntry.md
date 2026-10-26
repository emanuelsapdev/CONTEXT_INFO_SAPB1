# EDFImportEntry — Entrada de importación de documento electrónico

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Complex type:** `EDFImportEntry`
- **Descripción (ES):** Entrada de importación de documento electrónico
- **Description (EN):** EDF Import Entry

- **Properties:** 22

## Properties (22)

| # | Property | Type | Nullable | Description (EN) | Descripción (ES) |
|---|---|---|---|---|---|
| 1 | `AbsEntry` | Edm.Int32 | Yes | Abs Entry | Entrada absoluta (ID interno) |
| 2 | `Code` | [ElectronicDocProtocolCodeStrEnum](../Enums/ElectronicDocProtocolCodeStrEnum.md) | Yes | Code | Código |
| 3 | `Status` | [ElectronicDocumentEntryStatusEnum](../Enums/ElectronicDocumentEntryStatusEnum.md) | Yes | Status | Estado |
| 4 | `Message` | Edm.String | Yes | Message | Mensaje |
| 5 | `TestMode` | Edm.String | Yes | Test Mode | Modo de prueba |
| 6 | `GUID` | Edm.String | Yes | GUID | GUID |
| 7 | `Authority` | Edm.String | Yes | Authority | Autoridad |
| 8 | `ProcessingSource` | Edm.String | Yes | Processing Source | Origen del procesamiento |
| 9 | `MetaData` | Edm.String | Yes | Meta Data | Metadatos |
| 10 | `CreateDate` | Edm.DateTimeOffset | Yes | Create Date | Fecha de creación |
| 11 | `CreateTime` | Edm.Int32 | Yes | Create Time | Hora de creación |
| 12 | `UpdateDate` | Edm.DateTimeOffset | Yes | Update Date | Fecha de actualización |
| 13 | `UpdateTime` | Edm.Int32 | Yes | Update Time | Hora de actualización |
| 14 | `User` | Edm.Int32 | Yes | User | Usuario |
| 15 | `User2` | Edm.Int32 | Yes | User 2 | Usuario 2 |
| 16 | `MimeType` | Edm.String | Yes | Mime Type | Tipo MIME |
| 17 | `FileName` | Edm.String | Yes | File Name | Nombre del archivo |
| 18 | `AssignedID` | Edm.String | Yes | Assigned ID | ID asignado |
| 19 | `CardCode` | Edm.String | Yes | Card Code | Código del socio de negocios |
| 20 | `DocumentDate` | Edm.DateTimeOffset | Yes | Document Date | Fecha del documento |
| 21 | `ObjectType` | Edm.String | Yes | Object Type | Tipo de objeto |
| 22 | `IsBPManual` | [BoYesNoEnum](../Enums/BoYesNoEnum.md) | Yes | Is Business Partner Manual | Socio de negocios manual |

## Used by (service operations)

- [`ElectronicDocumentService_AddImportEntry`](../Servicios/ElectronicDocumentService.md#electronicdocumentservice_addimportentry)
