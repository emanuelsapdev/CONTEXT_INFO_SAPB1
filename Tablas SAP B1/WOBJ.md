# WOBJ - Object Wizard

- **Tabla:** WOBJ
- **Descripción:** Object Wizard
- **Cantidad de campos:** 44
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WOBJ.html

## Campos (44)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ObjCode` | Object Code | Int | 11 | - |  |  |
| 2 | `ObjName` | Object Name | nVarChar | 20 | - |  |  |
| 3 | `Category` | Category | VarChar | 1 | - | 2 | `2` = Noun<br>`3` = Operation<br>`4` = History<br>`1` = Abstract<br>`0` = Not Exists |
| 4 | `TableName` | TableName | nVarChar | 20 | - |  |  |
| 5 | `NOE` | NOE or form | VarChar | 1 | - | N | `Y` = Yes<br>`F` = Form<br>`N` = None |
| 6 | `ObjDesc` | Object Description | nVarChar | 254 | - |  |  |
| 7 | `FileName` | File Name | nVarChar | 254 | - |  |  |
| 8 | `Status` | Execution Status | VarChar | 1 | - | D | `R` = Ready<br>`P` = Postponed<br>`D` = Done |
| 9 | `ClassName` | Class Name | nVarChar | 100 | - |  |  |
| 10 | `AutoComp` | OnAutoComplete | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 11 | `Cancel` | OnCancel | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 12 | `CanUpdate` | OnCanUpdate | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 13 | `ChckDelet` | OnCheckDelete | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 14 | `Close1` | OnClose | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 15 | `Create1` | OnCreate | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 16 | `CreateDef` | OnCreateDefaults | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 17 | `Delete1` | OnDelete | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 18 | `GetByKey` | OnGetByKey | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 19 | `GetNextSer` | OnGetNextSerial | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 20 | `InitData` | OnInitData | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 21 | `InitFlow` | OnInitFlow | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 22 | `EndSucFlow` | OnEndSuccessfulFlow | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 23 | `IsValid` | OnIsValid | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 24 | `PutSignate` | OnPutSignature | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 25 | `UndoCancel` | OnUndoCancel | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 26 | `Update1` | OnUpdate | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 27 | `Upgrade` | OnUpgrade | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 28 | `YearTransf` | OnYearTransfer | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 29 | `AddLogEnt` | OnAddLogEntry | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 30 | `LogTable` | Log Table | nVarChar | 20 | - |  |  |
| 31 | `CanDisplay` | Can Display | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 32 | `UserSign` | User Signature | Int | 11 | - | -1 |  |
| 33 | `IsSeries` | Is Series | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 34 | `AddInVer` | Added in version | Int | 11 | - |  |  |
| 35 | `AbbrevIdx` | Index in abbreviation strl | Int | 11 | - |  |  |
| 36 | `DfaultForm` | Default form for DI permission | Int | 11 | - |  |  |
| 37 | `IsService` | Is Service | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 38 | `ExtraPerm` | Extra Permission for DI | Int | 11 | - |  |  |
| 39 | `StrlIndex` | String list index | nVarChar | 254 | - |  |  |
| 40 | `CanArchive` | Can Archive | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 41 | `CreateDate` | Creation date | Date | 8 | - |  |  |
| 42 | `CreateTime` | Creation Time | Int | 6 | - |  |  |
| 43 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 44 | `UpdateTime` | Update Time | Int | 6 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ObjCode |
| NAME | Yes | ObjName |
