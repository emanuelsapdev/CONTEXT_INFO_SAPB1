# OIMP - Import to Microsoft Excel

- **Tabla:** OIMP
- **Descripción:** Import to Microsoft Excel
- **Cantidad de campos:** 18
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OIMP.html

## Campos (18)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SessionId` | Session ID | Int | 11 | - |  |  |
| 2 | `ObjectType` | Business Object | Int | 6 | - |  |  |
| 3 | `FileObNam` | Mapped Business Object for the Uploaded File | nVarChar | 100 | - |  |  |
| 4 | `FileName` | Uploaded File Name | nVarChar | 100 | - |  |  |
| 5 | `DocName` | Uploaded Document Name | nVarChar | 100 | - |  |  |
| 6 | `FileHeader` | File Contains Header | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 7 | `MappingMtd` | Mapping Method | VarChar | 1 | - | M | `M` = Manual<br>`P` = Predefined Template<br>`S` = Saved Template |
| 8 | `SavedTempl` | Save Template Code | nVarChar | 100 | - |  |  |
| 9 | `RelatedObj` | Allow Related Object Creation | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 10 | `Status` | Status | VarChar | 1 | - |  | `P` = Parsing<br>`R` = Ready for Import<br>`I` = Import in Progress<br>`C` = Import Completed<br>`E` = Error in Import |
| 11 | `ImportOpt` | Import Option | nVarChar | 2 | - | IM | `IM` = Parent Object Only<br>`IS` = Child Object Only<br>`SP` = Parent and Child Objects<br>`SO` = Child Objects Only<br>`MP` = Parent and Child Objects<br>`MO` = Child Objects Only<br>`IO` = Import parent and child objects in one file |
| 12 | `ImportMtd` | Import Method | nVarChar | 2 | - | AO | `AU` = Add new records and update existing records<br>`AO` = Add new records without updating existing records<br>`UO` = Update existing records without adding new records |
| 13 | `ErrorOpt` | Error Option | nVarChar | 2 | - |  | `C` = Cancel import and perform rollback when one or more errors occur<br>`IA` = Ignore all errors and process valid records<br>`R` = Perform a rollback when the number of errors reaches or exceeds the defined threshold ({NumberOfErrors}).<br>`IU` = Ignore up to {No. defined in NumberOfErrors} errors and process valid records |
| 14 | `NumOfErr` | Number of Errors | Int | 11 | - |  |  |
| 15 | `CreateDate` | Created Date | Date | 8 | - |  |  |
| 16 | `UpdateDate` | Updated Date | Date | 8 | - |  |  |
| 17 | `CreatedBy` | Created by User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 18 | `UpdatedBy` | Updated By | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SessionId |
