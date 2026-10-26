# ITEM - Item Resource

- **Tabla:** ITEM
- **Descripción:** Item Resource
- **Cantidad de campos:** 71
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ITEM.html

## Campos (71)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Created` | Creation Date | Date | 8 | - |  |  |
| 2 | `Updated` | Update Date | Date | 8 | - |  |  |
| 3 | `Name` | Form Name | nVarChar | 64 | - |  |  |
| 4 | `Num` | Item Number | Int | 11 | - |  |  |
| 5 | `ItemType` | Item Type | Int | 11 | - |  | `4` = Button<br>`121` = Check box<br>`114` = Edit popup<br>`16` = Edit text<br>`118` = Extended edit<br>`99` = Folder<br>`101` = FwdBck button<br>`123` = Graph<br>`124` = Icon<br>`116` = Link button<br>`127` = Grid<br>`120` = Media<br>`103` = Multi page<br>`115` = Pane button<br>`104` = Pane popup<br>`117` = Picture<br>`98` = Pipe<br>`125` = Popup<br>`119` = Preview<br>`112` = Progress<br>`122` = Radio button<br>`100` = Rectangle<br>`113` = Select popup<br>`8` = Static text<br>`102` = ActiveX<br>`0` = User item<br>`129` = Button Combo |
| 6 | `Enabled` | Enabled | VarChar | 1 | - | 1 | `0` = No<br>`1` = Yes |
| 7 | `_Top` | Top | Int | 11 | - |  |  |
| 8 | `_Bottom` | Bottom | Int | 11 | - |  |  |
| 9 | `_Left` | Left | Int | 11 | - |  |  |
| 10 | `_Right` | Right | Int | 11 | - |  |  |
| 11 | `Font` | Font Number | Int | 11 | - |  |  |
| 12 | `FontSize` | Font Size | Int | 11 | - |  |  |
| 13 | `Attributes` | Attributes | Int | 11 | - |  |  |
| 14 | `Style` | Style | Int | 11 | - |  |  |
| 15 | `Mode` | Mode | Int | 11 | - |  |  |
| 16 | `VarNum` | Variable Number | Int | 11 | - |  |  |
| 17 | `AttrVar` | Attribute Variable | Int | 11 | - |  |  |
| 18 | `NewLineVar` | New Line Variable | Int | 11 | - |  |  |
| 19 | `ProcVar` | Proc Variable | Int | 11 | - |  |  |
| 20 | `LinkVar` | Link Variable | Int | 11 | - |  |  |
| 21 | `DragVar` | Drag Variable | Int | 11 | - |  |  |
| 22 | `FileCode` | Table Name | nVarChar | 20 | - |  |  |
| 23 | `FieldNum` | Field Alias | nVarChar | 10 | - |  |  |
| 24 | `Editable` | Editable | VarChar | 1 | - | 1 | `0` = No<br>`1` = Yes |
| 25 | `Invisible` | Invisible | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 26 | `SuppressZe` | Suppress Zeros | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 27 | `DfltButton` | Default Button | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 28 | `DataRequir` | Data Required | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 29 | `ForceUpper` | Force Upper | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 30 | `RightJust` | Right Justified | VarChar | 1 | - | 1 | `0` = No<br>`1` = Yes<br>`2` = Language dependant<br>`3` = Oppos Language |
| 31 | `UserType` | Data Binding Type | VarChar | 1 | - | 0 | `0` = Data<br>`1` = User Variable<br>`2` = Multiple Data Type |
| 32 | `ShowType` | Show type | VarChar | 1 | - | 0 | `0` = Value + Description<br>`1` = Value only<br>`2` = Description only |
| 33 | `DispDecr` | Display Description | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 34 | `TabOrder` | TAB Order | Int | 11 | - |  |  |
| 35 | `LinkTo` | Link to Item | Int | 11 | - |  |  |
| 36 | `DragEntity` | Drag Entity | Int | 11 | - |  |  |
| 37 | `FromPane` | From Pane | Int | 11 | - |  |  |
| 38 | `ToPane` | To Pane | Int | 11 | - |  |  |
| 39 | `Class` | Class | Int | 11 | - |  |  |
| 40 | `StrIndex` | String Index | Int | 11 | - | 0 |  |
| 41 | `HkeyIndex` | Hotkey Index | Int | 11 | - |  |  |
| 42 | `DescIndex` | Description Index | Int | 11 | - | 0 |  |
| 43 | `FrameRed` | Frame Red | Int | 11 | - |  |  |
| 44 | `FrameGreen` | Frame Green | Int | 11 | - |  |  |
| 45 | `FrameBlue` | Frame Blue | Int | 11 | - |  |  |
| 46 | `BodyRed` | Body Red | Int | 11 | - |  |  |
| 47 | `BodyGreen` | Body Green | Int | 11 | - |  |  |
| 48 | `BodyBlue` | Body Blue | Int | 11 | - |  |  |
| 49 | `TextRed` | Text Red | Int | 11 | - |  |  |
| 50 | `TextGreen` | Text Green | Int | 11 | - |  |  |
| 51 | `TextBlue` | Text Blue | Int | 11 | - |  |  |
| 52 | `ThumbRed` | Thumb Red | Int | 11 | - |  |  |
| 53 | `ThumbGreen` | Thumb Green | Int | 11 | - |  |  |
| 54 | `ThumbBlue` | Thumb Blue | Int | 11 | - |  |  |
| 55 | `TxtFgRed` | Text Foreground Red | Int | 11 | - |  |  |
| 56 | `TxtFgGreen` | Text Foreground Green | Int | 11 | - |  |  |
| 57 | `TxtFgBlue` | Text Foreground blue | Int | 11 | - |  |  |
| 58 | `TxtBgRed` | Text Background Red | Int | 11 | - |  |  |
| 59 | `TxtBgGreen` | Text Background Green | Int | 11 | - |  |  |
| 60 | `TxtBgBlue` | Text Background Blue | Int | 11 | - |  |  |
| 61 | `UniqueID` | Unique ID | nVarChar | 10 | - |  |  |
| 62 | `ItemString` | Item String | nVarChar | 254 | - |  |  |
| 63 | `ItemDesc` | Item Description | nVarChar | 254 | - |  |  |
| 64 | `HotkeyPos` | Hotkey Position | Int | 11 | - |  |  |
| 65 | `WrapText` | Wrap Text | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 66 | `UsrSgnStr` | User Sign For String Change | Int | 11 | - | -1 |  |
| 67 | `UsrSgnAttr` | User Sign For Attribs Change | Int | 11 | - | -1 |  |
| 68 | `FontName` | Font Name | nVarChar | 32 | - |  |  |
| 69 | `ResCode` | Resource Code from RSBD | Int | 11 | - | -1 |  |
| 70 | `RevCode` | Revision Code | Int | 11 | - | -1 |  |
| 71 | `BindObjId` | Bind Object Id | Int | 11 | - | -1 |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Name, Num, ResCode, RevCode |
| STRING | No | StrIndex |
| UNIQUE_ID | Yes | Name, UniqueID |
