# RAMI - RAMI

- **Tabla:** RAMI
- **Descripción:** RAMI
- **Cantidad de campos:** 24
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RAMI.html

## Campos (24)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ErrUID` | Error Message Unique ID | nVarChar | 11 | - |  |  |
| 2 | `StrlNum` | String List Number | Int | 11 | - |  |  |
| 3 | `StrIdx` | String Index | Int | 11 | - |  |  |
| 4 | `GuidStr` | GUID String | nVarChar | 32 | - | 3A51AF1A405C41479530D05FF95A3FBA |  |
| 5 | `MsgDef` | Message Define | nVarChar | 100 | - |  |  |
| 6 | `MsgType` | Message Type | VarChar | 1 | - | E | `E` = Error<br>`W` = Warning<br>`N` = Info<br>`S` = Success<br>`O` = None |
| 7 | `MsgArea` | Message Area | nVarChar | 20 | - | -1 | `-1`<br>`AP_AR` = Sales and Purchurse orders<br>`RPT` = Reports<br>`PROD` = Production<br>`LGST` = ItemMasterData<br>`INVT` = Inventory<br>`FIN` = Financial<br>`BANK` = Banking<br>`CARD` = BP Master Data<br>`AUTH` = Authorization<br>`ADMIN` = Administration<br>`SDK` = SDK UI<br>`LCNS` = License<br>`ADDON` = Add-On manager<br>`FORM` = Form Infrastructure<br>`DB` = DB Infrastructure<br>`CORE` = Core Layer<br>`INST` = Installation and Upgrade |
| 8 | `ScnExp` | Scenarion Explanation | Text | 16 | - |  |  |
| 9 | `ObjName` | Object Name | nVarChar | 20 | - |  |  |
| 10 | `SonTable` | Son Table | nVarChar | 20 | - |  |  |
| 11 | `Alias` | Alias | nVarChar | 10 | - |  |  |
| 12 | `FormID` | Form ID | Int | 11 | - |  |  |
| 13 | `PaneID` | Pane Id | Int | 6 | - | 0 |  |
| 14 | `ItemID` | Item ID | Int | 11 | - | -1 |  |
| 15 | `CreateDate` | Creation date | Date | 8 | - |  |  |
| 16 | `CreateTime` | Creation Time | Int | 6 | - |  |  |
| 17 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 18 | `UpdateTime` | Update Time | Int | 6 | - |  |  |
| 19 | `UserSign` | User Sign | Int | 11 | - |  |  |
| 20 | `SolExp` | Solution Explanation | Text | 16 | - |  |  |
| 21 | `CsnId` | CSN Note Id | nVarChar | 30 | - |  |  |
| 22 | `DispType` | Display Type | nVarChar | 30 | - | SBAR | `SBAR` = Sbar<br>`NOTE` = Note<br>`DIALOG_OKCancelType` = Dialog OK Cancel<br>`DIALOG_YesNoCancelType` = Dialog Yes No Cancel<br>`DIALOG_YesNoType` = Dialog Yes No<br>`DIALOG_YesAllNoAllCancelType` = Dialog Yes All No All Cancel<br>`DIALOG_ErrorOkType` = Dialog Error Ok<br>`DIALOG_ContinueSaveType` = Dialog Continue Save<br>`DIALOG_RemoveCancelType` = Dialog Remove Cancel<br>`DIALOG_ContinueCancelType` = Dialog Continue Cancel<br>`DIALOG_ContinueCancelNoType` = Dialog Continue Cancel No<br>`DIALOG_AddCancelType` = Dialog Add Cancel<br>`DIALOG_ContinueStopType` = Dialog Continue Stop<br>`DIALOG_YesCancelType` = Dialog Yes Cancel<br>`DIALOG_ContinueOpenType` = Dialog Continue Open<br>`DIALOG_OpenContinueCancelType` = Dialog Open Continue Cancel<br>`DIALOG_YesYesAllNoType` = Dialog Yes Yes All No<br>`DIALOG_YesYesAllNoAllType` = Dialog Yes Yes All No All |
| 23 | `ColmID` | Column ID | Int | 11 | - | -1 |  |
| 24 | `IsDeleted` | Is Deleted | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |

## Claves e índices (5)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ErrUID |
| GUID | No | GuidStr |
| CodeDefine | Yes | MsgDef |
| String | Yes | StrlNum, StrIdx |
| ObjectId | No | ObjName, SonTable, Alias |
