# OUDO - User-Defined Object

- **Tabla:** OUDO
- **Descripción:** User-Defined Object
- **Cantidad de campos:** 31
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OUDO.html

## Campos (31)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | nVarChar | 20 | - |  |  |
| 2 | `Name` | Name | nVarChar | 100 | - |  |  |
| 3 | `TableName` | Table Name | nVarChar | 19 | [OUTB](OUTB.md) |  |  |
| 4 | `LogTable` | Log Table Name | nVarChar | 20 | - |  |  |
| 5 | `TYPE` | Object Type | VarChar | 1 | - | 1 | `1` = Master Data<br>`3` = Document |
| 6 | `MngSeries` | Manage Series | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `CanDelete` | Delete | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 8 | `CanClose` | Close | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 9 | `CanCancel` | Cancel | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 10 | `ExtName` | Extension Name | nVarChar | 254 | - |  |  |
| 11 | `CanFind` | Find | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 12 | `CanYrTrnsf` | Year Transfer | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 13 | `CanDefForm` | Create Default Form | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 14 | `CanLog` | Log | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 15 | `OvrWrtDll` | Overwrite DLL File | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 16 | `UIDFormat` | Unique Form ID Format | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 17 | `CanArchive` | Archive | VarChar | 1 | - | N |  |
| 18 | `MenuItem` | Specify Menu Item | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 19 | `MenuCapt` | Menu Caption | nVarChar | 254 | - |  |  |
| 20 | `FatherMenu` | Parent Menu ID | Int | 11 | - |  |  |
| 21 | `Position` | Menu Position | Int | 6 | - |  |  |
| 22 | `CanNewForm` | Create Enhanced Form | VarChar | 1 | - | Y |  |
| 23 | `IsRebuild` | If Needed, Rebuild New Form | VarChar | 1 | - | Y |  |
| 24 | `NewFormSrf` | Enhanced Form: SRF File | Text | 16 | - |  |  |
| 25 | `MenuUid` | Menu UID | nVarChar | 32 | - |  |  |
| 26 | `LstUpdDate` | Last Update Date | Date | 8 | - |  |  |
| 27 | `LstUpdTime` | Last Update Time | Int | 11 | - |  |  |
| 28 | `CanApprove` | Approve | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 29 | `TemplateID` | Workflow Template ID | Int | 11 | [OWMG](OWMG.md) |  |  |
| 30 | `ApplyPerm` | Apply Authorization for UDO | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 31 | `EnableDPP` | Personal Data Protection | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
| TABLE | Yes | TableName |
