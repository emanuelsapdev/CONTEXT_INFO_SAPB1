# COLM - COLM resource

- **Tabla:** COLM
- **Descripción:** COLM resource
- **Cantidad de campos:** 64
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/COLM.html

## Campos (64)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Created` | Creation Date | Date | 8 | - |  |  |
| 2 | `Updated` | Update Date | Date | 8 | - |  |  |
| 3 | `Name` | Table Name | nVarChar | 64 | - |  |  |
| 4 | `Num` | Column Number | Int | 11 | - |  |  |
| 5 | `ItemType` | Item Type | Int | 11 | - | 0 | `0` = None<br>`16` = Edit text<br>`105` = Bar<br>`113` = Select popup<br>`116` = Link button<br>`121` = Check box<br>`117` = Picture |
| 6 | `Enabled` | Enabled | VarChar | 1 | - | 1 | `0` = No<br>`1` = Yes |
| 7 | `CellType` | Cell Type | Int | 11 | - | 16 | `0` = None<br>`16` = Edit text<br>`105` = Bar<br>`113` = Select popup<br>`116` = Link button<br>`121` = Check box<br>`117` = Picture |
| 8 | `Font` | Font Number | Int | 11 | - |  |  |
| 9 | `FontSize` | Font Size | Int | 11 | - |  |  |
| 10 | `Attributes` | Attributes | Int | 11 | - |  |  |
| 11 | `Style` | Style | Int | 11 | - |  |  |
| 12 | `Mode` | Mode | Int | 11 | - |  |  |
| 13 | `TitleType` | Title Type | Int | 11 | - | 0 | `0` = None<br>`117` = Picture |
| 14 | `TitleEnabl` | Title Enabled | VarChar | 1 | - |  |  |
| 15 | `TitleFont` | Title Font Number | Int | 11 | - |  |  |
| 16 | `TFontSize` | Title Font Size | Int | 11 | - |  |  |
| 17 | `TitleAtt` | Title Attributes | Int | 11 | - |  |  |
| 18 | `TitleStyle` | Title Style | Int | 11 | - |  |  |
| 19 | `TitleMode` | Title Mode | Int | 11 | - |  |  |
| 20 | `VarNum` | Variable Number | Int | 11 | - |  |  |
| 21 | `LinkVar` | Link Variable | Int | 11 | - |  |  |
| 22 | `DragVar` | Drag Variable | Int | 11 | - |  |  |
| 23 | `FileCode` | Table Code | nVarChar | 20 | - |  |  |
| 24 | `FieldNum` | Field Alias | nVarChar | 10 | - |  |  |
| 25 | `Editable` | Editable | VarChar | 1 | - | 1 | `0` = No<br>`1` = Yes |
| 26 | `SuppressZe` | Suppress Zeros | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 27 | `DataRequir` | Data Required | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 28 | `ForceUpper` | Force Upper | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 29 | `RightJust` | Right Justified | VarChar | 1 | - | 1 | `0` = No<br>`1` = Yes<br>`2` = Language dependant |
| 30 | `UserType` | Binding Type | VarChar | 1 | - | 0 | `0` = Data<br>`1` = User Variable |
| 31 | `Sentence` | Sentencing | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 32 | `ShowType` | Show Type | VarChar | 1 | - | 0 | `0` = Value + Description<br>`1` = Value only<br>`2` = Description only |
| 33 | `DispDecr` | Display Description | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 34 | `LinkTo` | Link To Item | Int | 11 | - |  |  |
| 35 | `DragEntity` | Drag Entity | Int | 11 | - |  |  |
| 36 | `Class` | Class | Int | 11 | - |  |  |
| 37 | `TitleIndex` | Title Index | Int | 11 | - | 0 |  |
| 38 | `DescIndex` | Description Index | Int | 11 | - | 0 |  |
| 39 | `TxtFgRed` | Text Foreground Red | Int | 11 | - |  |  |
| 40 | `TxtFgGreen` | Text Foreground Green | Int | 11 | - |  |  |
| 41 | `TxtFgBlue` | Text Foreground Blue | Int | 11 | - |  |  |
| 42 | `TxtBgRed` | Text Background Red | Int | 11 | - |  |  |
| 43 | `TxtBgGreen` | Text Background Green | Int | 11 | - |  |  |
| 44 | `TxtBgBlue` | Text Background Blue | Int | 11 | - |  |  |
| 45 | `TtlFgRed` | Title Foreground Red | Int | 11 | - |  |  |
| 46 | `TtlFgGreen` | Title Foreground Green | Int | 11 | - |  |  |
| 47 | `TtlFgBlue` | Title Foreground Blue | Int | 11 | - |  |  |
| 48 | `TtlBgRed` | Title Background Red | Int | 11 | - |  |  |
| 49 | `TtlBgGreen` | Title Background Green | Int | 11 | - |  |  |
| 50 | `TtlBgBlue` | Title Background Blue | Int | 11 | - |  |  |
| 51 | `Width` | Width | Int | 11 | - |  |  |
| 52 | `SuppRepeat` | Suppress Repeating | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 53 | `AutoGraph` | Auto Graph | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 54 | `AutoCumm` | Auto Cummulative | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 55 | `UniqueID` | Unique ID | nVarChar | 10 | - |  |  |
| 56 | `TitleStr` | Title String | nVarChar | 254 | - |  |  |
| 57 | `ColDesc` | Column Description | nVarChar | 254 | - |  |  |
| 58 | `UsrSgnStr` | User Sign For Strings Change | Int | 11 | - | -1 |  |
| 59 | `UsrSgnAttr` | User Sign For Attribs Change | Int | 11 | - | -1 |  |
| 60 | `TtlFntName` | Title Font Name | nVarChar | 32 | - |  |  |
| 61 | `CllFntName` | Cell Font Name | nVarChar | 32 | - |  |  |
| 62 | `ResCode` | Resource Code from RSBD | Int | 11 | - | -1 |  |
| 63 | `RevCode` | Revision Code | Int | 11 | - | -1 |  |
| 64 | `BindObjId` | Bind Object Id | Int | 11 | - | -1 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Name, Num, ResCode, RevCode |
| UNIQUE_ID | Yes | Name, UniqueID |
