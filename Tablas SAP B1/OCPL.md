# OCPL - Quick Copy Log Manager

- **Tabla:** OCPL
- **Descripción:** Quick Copy Log Manager
- **Cantidad de campos:** 15
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OCPL.html

## Campos (15)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `StartDate` | Start Date | Date | 8 | - |  |  |
| 3 | `StartTime` | Start Time | nVarChar | 6 | - |  |  |
| 4 | `EndDate` | End Date | Date | 8 | - |  |  |
| 5 | `EndTime` | End Time | nVarChar | 6 | - |  |  |
| 6 | `CopySource` | Copy Source | nVarChar | 254 | - |  |  |
| 7 | `CopyTarget` | Copy Target | nVarChar | 254 | - |  |  |
| 8 | `UserName` | User Name | nVarChar | 20 | - |  |  |
| 9 | `CopyMethod` | Copy Method | Int | 6 | - |  | `2` = Delete All Records Then Add New Records<br>`4` = Update Existing Records Without Adding New Records<br>`8` = Add New Records Without Updating Existing Records<br>`16` = Add New Records and Update Existing Records<br>`0` = N/A |
| 10 | `FailRpn` | Copy failed | Int | 6 | - |  | `1` = Ignore All Errors and Copy Valid Records<br>`2` = Obtain User Confirmation<br>`3` = Terminate Copy Process When One or More Errors Occur<br>`4` = Terminate Copy Process When Number of Errors Exceeds |
| 11 | `MissingUDF` | UDF missing | VarChar | 1 | - |  | `2` = N/A<br>`1` = Copy Records and Ignore Missing UDFs<br>`0` = Do Not Copy Records with Missing UDFs |
| 12 | `CopyType` | Copy Type | Int | 6 | - |  |  |
| 13 | `ErrorNum` | Error Number | nVarChar | 11 | - |  |  |
| 14 | `NullifyAct` | Nullify Account | Int | 6 | - |  | `2` = N/A<br>`1` = Use Default Accounts in Target<br>`0` = Use Accounts in Source |
| 15 | `CopyEmtVal` | Copy Empty Value | Int | 6 | - |  | `2` = N/A<br>`1` = Do Not Overwrite Target Fields and Keep Original Values<br>`0` = Overwrite Target Fields with Empty Values |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
