# OHMM - SAP HANA Model Management

- **Tabla:** OHMM
- **Descripción:** SAP HANA Model Management
- **Cantidad de campos:** 17
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OHMM.html

## Campos (17)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `ModelAuth` | Model Author | nVarChar | 100 | - |  |  |
| 3 | `ModelName` | Model Name | nVarChar | 100 | - |  |  |
| 4 | `ModelVer` | Model Version | nVarChar | 100 | - |  |  |
| 5 | `Desc` | Description | Text | 16 | - |  |  |
| 6 | `Status` | Status | VarChar | 1 | - |  | `I` = Imported<br>`D` = Deployed<br>`T` = In Task |
| 7 | `InfoFile` | Info File | Text | 16 | - |  |  |
| 8 | `UpdateBy` | Last Updated User's Code | Int | 11 | - |  |  |
| 9 | `ChangeBy` | Last Changed SAP HANA User | nVarChar | 100 | - |  |  |
| 10 | `CreateDate` | Created at Date | nVarChar | 100 | - |  |  |
| 11 | `CreateTime` | Created at Time | Int | 11 | - |  |  |
| 12 | `ChangeDate` | Changed at Date | nVarChar | 100 | - |  |  |
| 13 | `ChangeTime` | Changed at Time | Int | 11 | - |  |  |
| 14 | `TaskId` | Task ID | Int | 11 | - |  |  |
| 15 | `DeployDate` | Deployment Date | Date | 8 | - |  |  |
| 16 | `DeployTime` | Deployment Time | Int | 11 | - |  |  |
| 17 | `Language` | Deployment Language | nVarChar | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry |
