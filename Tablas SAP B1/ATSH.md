# ATSH - Time Sheet - Header - History

- **Tabla:** ATSH
- **Descripción:** Time Sheet - Header - History
- **Cantidad de campos:** 24
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ATSH.html

## Campos (24)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | - |  |  |
| 2 | `ProjectID` | Project No. | Int | 11 | [OPMG](OPMG.md) |  |  |
| 3 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 4 | `Type` | Type | VarChar | 1 | - | E | `E` = Employee<br>`U` = User<br>`O` = External |
| 5 | `UserID` | Employee/User ID | Int | 11 | [OHEM](OHEM.md) |  |  |
| 6 | `LastName` | Last Name | nVarChar | 50 | - |  |  |
| 7 | `FirstName` | First Name | nVarChar | 50 | - |  |  |
| 8 | `Department` | Department | Int | 6 | - |  |  |
| 9 | `DateFrom` | Date From | Date | 8 | - |  |  |
| 10 | `DateTo` | Date To | Date | 8 | - |  |  |
| 11 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 12 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 13 | `UserSign` | User Signature | Int | 6 | - |  |  |
| 14 | `UserSign2` | Updating User | Int | 6 | - |  |  |
| 15 | `CreateDate` | Production Date | Date | 8 | - |  |  |
| 16 | `UpdateTS` | Update Full Time | Int | 11 | - |  |  |
| 17 | `DPPStatus` | Data Protection Status | VarChar | 1 | - | N | `N` = None<br>`D` = Erased |
| 18 | `SAPPassprt` | Extended SAP Passport | Text | 16 | - |  |  |
| 19 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 20 | `AtcEntry` | Attachment Entry | Int | 11 | [OATC](OATC.md) |  |  |
| 21 | `Attachment` | Attachment | Text | 16 | - |  |  |
| 22 | `UserCode` | Employee/User Code | nVarChar | 50 | - |  |  |
| 23 | `DataVers` | Data Version | Int | 11 | - | 1 |  |
| 24 | `OwnerCode` | Owner | Int | 11 | [OHEM](OHEM.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LogInstanc |
