# RITM - Reporting Element

- **Tabla:** RITM
- **Descripción:** Reporting Element
- **Cantidad de campos:** 88
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RITM.html

## Campos (88)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocCode` | Report | nVarChar | 8 | [RDOC](RDOC.md) |  |  |
| 2 | `ItemId` | Item ID | Int | 6 | - |  |  |
| 3 | `Container` | Parent Type | Int | 6 | - |  |  |
| 4 | `Type` | Type | Int | 6 | - |  | `1` = Page Header<br>`2` = Start of Report<br>`3` = Repetitive Area Header<br>`4` = Repetitive Area<br>`5` = Repetitive Area Footer<br>`6` = End of Report<br>`7` = Page Footer<br>`10` = Text Field<br>`11` = Picture Field<br>`12` = User Field |
| 5 | `VISIBLE` | Visible | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 6 | `SupZeros` | Suppress Zeros | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `ItemLeft` | Left Item | Int | 6 | - |  |  |
| 8 | `ItemTop` | Top | Int | 6 | - |  |  |
| 9 | `Width` | Width | Int | 6 | - |  |  |
| 10 | `Height` | Height | Int | 6 | - |  |  |
| 11 | `LMargin` | Left Margin | Int | 6 | - | 0 |  |
| 12 | `RMargin` | Right Margin | Int | 6 | - | 0 |  |
| 13 | `TMargin` | Top Margin | Int | 6 | - | 0 |  |
| 14 | `BMargin` | Bottom Margin | Int | 6 | - | 0 |  |
| 15 | `LeftLine` | Left Border Line Thickness | Int | 6 | - | 0 |  |
| 16 | `RightLine` | Right Border Line Thickness | Int | 6 | - | 0 |  |
| 17 | `TopLine` | Top Border Line Thickness | Int | 6 | - | 0 |  |
| 18 | `BottomLine` | Bottom Border Line Thickness | Int | 6 | - | 0 |  |
| 19 | `Shadow` | Shadow Thickness | Int | 6 | - | 0 |  |
| 20 | `BGRed` | Background - Red | Int | 11 | - | 255 |  |
| 21 | `BGGreen` | Background - Green | Int | 11 | - | 255 |  |
| 22 | `BGBlue` | Background - Blue | Int | 11 | - | 255 |  |
| 23 | `FGRed` | Text - Red | Int | 11 | - | 0 |  |
| 24 | `FGGreen` | Text - Green | Int | 11 | - | 0 |  |
| 25 | `FGBlue` | Text - Blue | Int | 11 | - | 0 |  |
| 26 | `MrkrRed` | Bold - Red | Int | 11 | - | 255 |  |
| 27 | `MrkrGreen` | Bold - Green | Int | 11 | - | 255 |  |
| 28 | `MrkrBlue` | Bold - Blue | Int | 11 | - | 255 |  |
| 29 | `BrdrRed` | Border - Red | Int | 11 | - | 0 |  |
| 30 | `BrdrGreen` | Border - Green | Int | 11 | - | 0 |  |
| 31 | `BrdrBlue` | Border - Blue | Int | 11 | - | 0 |  |
| 32 | `FromPane` | From Area | Int | 6 | - | 0 |  |
| 33 | `ToPane` | To Area | Int | 6 | - | 0 |  |
| 34 | `ItemGroup` | Group No. | Int | 6 | - | 0 |  |
| 35 | `FontName` | Font Name | nVarChar | 50 | - | Arial |  |
| 36 | `FontSize` | Font Size | Int | 6 | - | 12 |  |
| 37 | `TextStyle` | Text Style | Int | 11 | - | 0 |  |
| 38 | `Justific` | Horizontal Justification | Int | 6 | - | 2 | `1` = Right<br>`2` = Left<br>`3` = Centralized<br>`4` = Language-Dependent |
| 39 | `WRAP` | Segment | Int | 6 | - | 2 | `0` = Allow Overflow<br>`1` = Adjust to Cell<br>`2` = Divide into Rows |
| 40 | `PictSize` | Picture Size | Int | 6 | - | 0 | `0` = Original Size<br>`1` = Fit Field Size Non-Proportionally<br>`2` = Fit Field Size Proportionally<br>`3` = Fit Field Height<br>`4` = Fit Fields Width |
| 41 | `DataSource` | Data Source | Int | 6 | - | 1 | `1` = Static<br>`2` = Variable<br>`3` = Data<br>`4` = Calculation |
| 42 | `ItemStr` | String | Text | 16 | - |  |  |
| 43 | `VarNum` | Variable No. | Int | 6 | - |  |  |
| 44 | `FileName` | File Name | nVarChar | 20 | - |  |  |
| 45 | `FieldNum` | Field No. | nVarChar | 52 | - |  |  |
| 46 | `ShowDescr` | Display Description | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 47 | `CalcType` | Calculation Type | nVarChar | 2 | - | 1 | `0` = Formula<br>`1` = Page Number<br>`17` = Total Pages<br>`2` = Date<br>`3` = Time<br>`4` = Column Total<br>`5` = Column Average<br>`6` = General Row No.<br>`7` = Group Row No.<br>`8` = Sort Field Name<br>`9` = Sort Field Content<br>`10` = Continue<br>`11` = Continued on Next Page<br>`12` = Generation Message<br>`13` = Column Summary for Page<br>`14` = Column Average for Page<br>`15` = Column Summary for Report<br>`16` = Column Average for Report |
| 48 | `ChangFlags` | Changeable | Int | 11 | - |  |  |
| 49 | `ApplID` | Item No. | Int | 6 | - |  |  |
| 50 | `CalcCol` | Calculation Column | Int | 6 | - |  |  |
| 51 | `YJustific` | Vertical Alignment | Int | 6 | - | 3 | `1` = Top<br>`2` = Bottom<br>`3` = Centralized |
| 52 | `SortLevel` | Sort Level | Int | 6 | - | 0 |  |
| 53 | `RevOrder` | Reverse Sort | VarChar | 1 | - | N | `Y` = Descending<br>`N` = Ascending |
| 54 | `SortType` | Sort Type | Int | 6 | - | 0 | `0` = Alpha<br>`1` = Numeric<br>`2` = Currency<br>`3` = Date |
| 55 | `IsUnique` | Unique | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 56 | `IsGroup` | Set as Group | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 57 | `NewPage` | New Page | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 58 | `BarCode` | Print as Bar Code | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 59 | `Condition` | Condition | Text | 16 | - |  |  |
| 60 | `LinkTo` | Link to Field | nVarChar | 20 | - |  |  |
| 61 | `Operator1` | Operator 1 | Int | 6 | - |  |  |
| 62 | `Operator2` | Operator 2 | Int | 6 | - |  |  |
| 63 | `Operation` | Operation | Int | 6 | - | 0 | `0`<br>`1` = +<br>`2` = -<br>`3` = x<br>`4` = /<br>`5` = %<br>`17` = Left Part (Characters)<br>`18` = Right Part (Mantissa)<br>`19` = Round<br>`6` = $Concat<br>`7` = $Right<br>`8` = $Left<br>`9` = $Sentence<br>`16` = $Length<br>`20` = $Currency<br>`21` = $Number<br>`10` = Less than<br>`11` = Less or Equal<br>`12` = Equal<br>`13` = Not equal<br>`14` = Greater or Equal<br>`15` = Greater than |
| 64 | `BCStandard` | Bar Code Standard | Int | 6 | - | 0 | `0` = EAN-13<br>`1` = Code 39<br>`2` = Code 128 |
| 65 | `SumInWords` | Display Total as a Word | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 66 | `ExcFonting` | Block Font Change | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 67 | `StrIndex` | String Index | Int | 11 | - | 0 |  |
| 68 | `ContIndex` | Container Index | Int | 6 | - | 0 |  |
| 69 | `ItemIndex` | Item Index | Int | 6 | - | 0 |  |
| 70 | `StrLength` | String Length | Int | 6 | - |  |  |
| 71 | `StrFiller` | String Filler | VarChar | 1 | - |  |  |
| 72 | `RelatedTo` | Link to Field | nVarChar | 20 | - |  |  |
| 73 | `NextSeg` | Next Segment Item Number | nVarChar | 20 | - |  |  |
| 74 | `HightAdjst` | Height Adjustments | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 75 | `DupRpttAre` | Duplicate Repetitive Area | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 76 | `LnsRpttAre` | No. of Rows in Repetitive Area | Int | 11 | - | 0 |  |
| 77 | `RptDupDist` | Distance To Rptt Dup. (pixels) | Int | 11 | - | 0 |  |
| 78 | `FieldId` | Unique ID | nVarChar | 20 | - |  |  |
| 79 | `FGEnabled` | Grid Enabled | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 80 | `BGEnabled` | Background Enabled | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 81 | `MKEnabled` | Highlight Enabled | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 82 | `BDEnabled` | Frame Enabled | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 83 | `HidEmpRptt` | Hide Empty Area | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 84 | `RpttFtrAll` | Display Rep. Footer on All | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 85 | `GbiDataTyp` | Data Type | Int | 6 | - | 0 | `0`<br>`1` = C n<br>`2` = C.. n<br>`3` = I.. n<br>`4` = D w.d |
| 86 | `GbiDataLen` | Data Length | nVarChar | 6 | - |  |  |
| 87 | `PageBreak` | Page Break | Int | 6 | - | 0 | `0` = None<br>`1` = Before Area<br>`2` = After Area |
| 88 | `IsLogo` | Is Logo | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (4)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocCode, ItemId |
| CONTAINER | No | DocCode, Container, ContIndex, ItemGroup |
| APPL_ID | No | DocCode, ApplID |
| TYPE | No | DocCode, Type, ItemIndex |
