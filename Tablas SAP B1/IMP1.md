# IMP1 - History Table

- **Tabla:** IMP1
- **Descripción:** History Table
- **Cantidad de campos:** 11
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/IMP1.html

## Campos (11)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SessionId` | Session ID | Int | 11 | - |  |  |
| 2 | `ObjectType` | Business Object | Int | 6 | - |  |  |
| 3 | `Status` | Status | VarChar | 1 | - |  | `P` = Parsing<br>`R` = Ready for Import<br>`I` = Import in Progress<br>`C` = Import Completed<br>`E` = Error in Import |
| 4 | `ImportOpt` | Import Option | VarChar | 1 | - |  | `M` = Import Main Object<br>`S` = Import Sub-Objects<br>`D` = Import main and sub-objects in separate files<br>`O` = Import main and sub-objects in one file |
| 5 | `ImportMtd` | Import Method | nVarChar | 2 | - | AO | `AU` = Add new records and update existing records<br>`AO` = Add new records without updating existing records<br>`UO` = Update existing records without adding new records |
| 6 | `ErrorOpt` | Error Option | nVarChar | 2 | - |  | `C` = Cancel import and perform rollback when one or more errors occur<br>`IA` = Ignore all errors and process valid records<br>`R` = Perform a rollback when the number of errors reaches or exceeds the defined threshold ({NumberOfErrors}).<br>`IU` = Ignore up to {No. defined in NumberOfErrors} errors and process valid records |
| 7 | `NumOfErr` | Number of Errors | Int | 11 | - |  |  |
| 8 | `CreateDate` | Created Date | Date | 8 | - |  |  |
| 9 | `UpdateDate` | Updated Date | Date | 8 | - |  |  |
| 10 | `CreatedBy` | Created by User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 11 | `UpdatedBy` | Updated By | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SessionId |
