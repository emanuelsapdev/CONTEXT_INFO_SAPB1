# RMTL - MITL resource

- **Tabla:** RMTL
- **Descripción:** MITL resource
- **Cantidad de campos:** 70
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RMTL.html

## Campos (70)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Created` | Creation date | Date | 8 | - |  |  |
| 2 | `Updated` | Update date | Date | 8 | - |  |  |
| 3 | `Language` | Language code | Int | 11 | - |  |  |
| 4 | `Name` | MITL name | nVarChar | 64 | - |  |  |
| 5 | `Num` | Column number | Int | 11 | - |  |  |
| 6 | `ItemType` | Item type | Int | 11 | - | 0 | `0` = None<br>`16` = Edit text<br>`105` = Bar<br>`113` = Select popup<br>`116` = Link button<br>`121` = Check box<br>`117` = Picture |
| 7 | `Enabled` | Enabled | VarChar | 1 | - | 1 | `0` = No<br>`1` = Yes |
| 8 | `CellType` | CellType | Int | 11 | - | 16 | `0` = None<br>`16` = Edit text<br>`105` = Bar<br>`113` = Select popup<br>`116` = Link button<br>`121` = Check box |
| 9 | `CellRes` | Cell resource | Int | 11 | - |  |  |
| 10 | `Font` | Font number | Int | 11 | - |  |  |
| 11 | `FontSize` | Font size | Int | 11 | - |  |  |
| 12 | `Attributes` | Attributes | Int | 11 | - |  |  |
| 13 | `Style` | Style | Int | 11 | - |  |  |
| 14 | `Mode` | Mode | Int | 11 | - |  |  |
| 15 | `TitleType` | Title type | Int | 11 | - | 0 | `0` = None<br>`117` = Picture |
| 16 | `TitleEnabl` | Title enabled | VarChar | 1 | - |  |  |
| 17 | `TitleRes` | Title resource | Int | 11 | - |  |  |
| 18 | `TitleFont` | Title font number | Int | 11 | - |  |  |
| 19 | `TFontSize` | Title font size | Int | 11 | - |  |  |
| 20 | `TitleAttr` | Title attributes | Int | 11 | - |  |  |
| 21 | `TitleStyle` | Title style | Int | 11 | - |  |  |
| 22 | `TitleMode` | Title mode | Int | 11 | - |  |  |
| 23 | `VarNum` | Variable number | Int | 11 | - |  |  |
| 24 | `LinkVar` | Link variable | Int | 11 | - |  |  |
| 25 | `DragVar` | Drag variable | Int | 11 | - |  |  |
| 26 | `FileCode` | File code | nVarChar | 8 | - |  |  |
| 27 | `FieldNum` | Field number | Int | 11 | - |  |  |
| 28 | `IndexType` | Index type | VarChar | 1 | - | 0 | `0` = Variable<br>`1` = Static |
| 29 | `IndexVal` | Index value | Int | 11 | - |  |  |
| 30 | `FatIdxType` | Father index type | VarChar | 1 | - | 0 | `0` = Variable<br>`1` = Static |
| 31 | `FatIdxVal` | Father index value | Int | 11 | - |  |  |
| 32 | `Editable` | Editable | VarChar | 1 | - | 1 | `0` = No<br>`1` = Yes |
| 33 | `SuppressZe` | Suppress zeros | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 34 | `DataRequir` | Data required | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 35 | `ForceUpper` | Force upper | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 36 | `RightJust` | Right justified | VarChar | 1 | - | 1 | `0` = No<br>`1` = Yes |
| 37 | `UserType` | User type | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 38 | `Sentence` | Sentencing | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 39 | `ShowType` | Show type | VarChar | 1 | - | 0 | `0` = Value + Description<br>`1` = Value only<br>`2` = Description only |
| 40 | `DispDecr` | Display description | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 41 | `LinkTo` | Link to item | Int | 11 | - |  |  |
| 42 | `DragEntity` | Drag entity | Int | 11 | - |  |  |
| 43 | `Class` | Class | Int | 11 | - |  |  |
| 44 | `ItemString` | Item string | nVarChar | 64 | - |  |  |
| 45 | `StringUpd` | String update date | Date | 8 | - |  |  |
| 46 | `StringLen` | String length | Int | 11 | - |  |  |
| 47 | `Title` | Title string | nVarChar | 64 | - |  |  |
| 48 | `TitleUpd` | Title updated | Date | 8 | - |  |  |
| 49 | `TitleLen` | Title length | Int | 11 | - |  |  |
| 50 | `ItemDesc` | Item description | nVarChar | 30 | - |  |  |
| 51 | `DescUpd` | Description update date | Date | 8 | - |  |  |
| 52 | `DescLen` | Description length | Int | 11 | - |  |  |
| 53 | `TxtFgRed` | Text foreground red | Int | 11 | - |  |  |
| 54 | `TxtFgGreen` | Text foreground green | Int | 11 | - |  |  |
| 55 | `TxtFgBlue` | Text foreground blue | Int | 11 | - |  |  |
| 56 | `TxtBgRed` | Text background red | Int | 11 | - |  |  |
| 57 | `TxtBgGreen` | Text background green | Int | 11 | - |  |  |
| 58 | `TxtBgBlue` | Text background green | Int | 11 | - |  |  |
| 59 | `TtlFgRed` | Title foreground red | Int | 11 | - |  |  |
| 60 | `TtlFgGreen` | Title foreground green | Int | 11 | - |  |  |
| 61 | `TtlFgBlue` | Title foreground blue | Int | 11 | - |  |  |
| 62 | `TtlBgRed` | Title background red | Int | 11 | - |  |  |
| 63 | `TtlBgGreen` | Title background green | Int | 11 | - |  |  |
| 64 | `TtlBgBlue` | Title background blue | Int | 11 | - |  |  |
| 65 | `Width` | Width | Int | 11 | - |  |  |
| 66 | `UserLen` | User length | Int | 11 | - |  |  |
| 67 | `SuppRepeat` | Suppress repeating | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 68 | `AutoGraph` | Auto graph | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 69 | `AutoCumm` | Auto cummulative | VarChar | 1 | - | 0 | `0` = No<br>`1` = Yes |
| 70 | `UniqueID` | Unique ID | nVarChar | 10 | - |  |  |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Language, Name, Num |
| M_NAME | No | Name, Num |
| UNIQUE_ID | Yes | Language, Name, UniqueID |
