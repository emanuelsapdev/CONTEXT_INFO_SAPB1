# RFTL - FITL resource

- **Tabla:** RFTL
- **Descripción:** FITL resource
- **Cantidad de campos:** 72
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RFTL.html

## Campos (72)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Created` | Creation date | Date | 8 | - |  |  |
| 2 | `Updated` | Update dateS | Date | 8 | - |  |  |
| 3 | `Language` | Language code | Int | 11 | - |  |  |
| 4 | `Name` | FITL name | nVarChar | 64 | - |  |  |
| 5 | `Num` | Item number | Int | 11 | - |  |  |
| 6 | `ItemType` | Item type | Int | 11 | - |  | `4` = Button<br>`121` = Check box<br>`114` = Edit popup<br>`16` = Edit text<br>`118` = Extended edit<br>`99` = Folder<br>`101` = FwdBck button<br>`123` = Graph<br>`124` = Icon<br>`116` = Link button<br>`127` = Matrix<br>`120` = Media<br>`103` = Multi page<br>`115` = Pane button<br>`104` = Pane popup<br>`117` = Picture<br>`98` = Pipe<br>`125` = Popup<br>`119` = Preview<br>`112` = Progress<br>`122` = Radio button<br>`100` = Rectangle<br>`113` = Select popup<br>`8` = Static text<br>`102` = User group<br>`0` = User item |
| 7 | `Enabled` | Enabled | VarChar | 1 | - | 1 | `0` = No<br>`1` = Yes |
| 8 | `_Top` | Top | Int | 11 | - |  |  |
| 9 | `_Bottom` | Bottom | Int | 11 | - |  |  |
| 10 | `_Left` | Left | Int | 11 | - |  |  |
| 11 | `_Right` | Right | Int | 11 | - |  |  |
| 12 | `ItemRes` | Item resource | Int | 11 | - |  |  |
| 13 | `Font` | Font number | Int | 11 | - |  |  |
| 14 | `FontSize` | Font size | Int | 11 | - |  |  |
| 15 | `Attributes` | Attributes | Int | 11 | - |  |  |
| 16 | `Style` | Style | Int | 11 | - |  |  |
| 17 | `Mode` | Mode | Int | 11 | - |  |  |
| 18 | `VarNum` | Variable number | Int | 11 | - |  |  |
| 19 | `AttrVar` | Attribute variable | Int | 11 | - |  |  |
| 20 | `NewLineVar` | New line variable | Int | 11 | - |  |  |
| 21 | `ProcVar` | Proc variable | Int | 11 | - |  |  |
| 22 | `LinkVar` | Link variable | Int | 11 | - |  |  |
| 23 | `DragVar` | Drag variable | Int | 11 | - |  |  |
| 24 | `FileCode` | File code | nVarChar | 8 | - |  |  |
| 25 | `FieldNum` | Field number | Int | 11 | - |  |  |
| 26 | `IndexType` | Index type | VarChar | 1 | - | 0 | `0` = Variable<br>`1` = Static |
| 27 | `IndexVal` | Index value | Int | 11 | - |  |  |
| 28 | `FatIdxType` | Father index type | VarChar | 1 | - | 0 | `0` = Variable<br>`1` = Static |
| 29 | `FatIdxVal` | Father index value | Int | 11 | - |  |  |
| 30 | `Editable` | Editable | VarChar | 1 | - | 1 | `0` = No<br>`1` = Yes |
| 31 | `Invisible` | Invisible | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 32 | `SuppressZe` | Suppress zeros | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 33 | `DfltButton` | Default button | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 34 | `DataRequir` | Data required | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 35 | `ForceUpper` | Force upper | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 36 | `RightJust` | Right justified | VarChar | 1 | - | 1 | `0` = No<br>`1` = Yes |
| 37 | `UserType` | User type | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 38 | `Override` | Override validation | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 39 | `Sentence` | Sentencing | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 40 | `ShowType` | Show type | VarChar | 1 | - | 0 | `0` = Value + Description<br>`1` = Value only<br>`2` = Description only |
| 41 | `DispDecr` | Display description | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 42 | `TabOrder` | TAB order | Int | 11 | - |  |  |
| 43 | `LinkTo` | Link to item | Int | 11 | - |  |  |
| 44 | `DragEntity` | Drag entity | Int | 11 | - |  |  |
| 45 | `FromPane` | From pane | Int | 11 | - |  |  |
| 46 | `ToPane` | To pane | Int | 11 | - |  |  |
| 47 | `Class` | Class | Int | 11 | - |  |  |
| 48 | `ItemString` | Item string | nVarChar | 64 | - |  |  |
| 49 | `StringUpd` | String update date | Date | 8 | - |  |  |
| 50 | `StringLen` | String length | Int | 11 | - |  |  |
| 51 | `ItemDesc` | Item description | nVarChar | 30 | - |  |  |
| 52 | `DescUpd` | Description update date | Date | 8 | - |  |  |
| 53 | `DescLen` | Description length | Int | 11 | - |  |  |
| 54 | `FrameRed` | Frame red | Int | 11 | - |  |  |
| 55 | `FrameGreen` | Frame green | Int | 11 | - |  |  |
| 56 | `FrameBlue` | Frame blue | Int | 11 | - |  |  |
| 57 | `BodyRed` | Body red | Int | 11 | - |  |  |
| 58 | `BodyGreen` | Body green | Int | 11 | - |  |  |
| 59 | `BodyBlue` | Body blue | Int | 11 | - |  |  |
| 60 | `TextRed` | Text red | Int | 11 | - |  |  |
| 61 | `TextGreen` | Text green | Int | 11 | - |  |  |
| 62 | `TextBlue` | Text blue | Int | 11 | - |  |  |
| 63 | `ThumbRed` | Thumb red | Int | 11 | - |  |  |
| 64 | `ThumbGreen` | Thumb green | Int | 11 | - |  |  |
| 65 | `ThumbBlue` | Thumb blue | Int | 11 | - |  |  |
| 66 | `TxtFgRed` | Text foreground red | Int | 11 | - |  |  |
| 67 | `TxtFgGreen` | Text foreground green | Int | 11 | - |  |  |
| 68 | `TxtFgBlue` | Text foreground blue | Int | 11 | - |  |  |
| 69 | `TxtBgRed` | Text background red | Int | 11 | - |  |  |
| 70 | `TxtBgGreen` | Text background green | Int | 11 | - |  |  |
| 71 | `TxtBgBlue` | Text background green | Int | 11 | - |  |  |
| 72 | `UniqueID` | Unique ID | nVarChar | 10 | - |  |  |

## Claves e índices (4)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Language, Name, Num |
| M_NAME | No | Name, Num |
| STRING | No | ItemString |
| UNIQUE_ID | Yes | Language, Name, UniqueID |
