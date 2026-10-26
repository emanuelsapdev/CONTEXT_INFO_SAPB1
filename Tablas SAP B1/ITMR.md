# ITMR - ITMR

- **Tabla:** ITMR
- **Descripción:** ITMR
- **Cantidad de campos:** 102
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ITMR.html

## Campos (102)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocCode` | Report | nVarChar | 8 | - |  |  |
| 2 | `ItemId` | Item ID | Int | 6 | - |  |  |
| 3 | `Container` | Parent Type | Int | 6 | - |  |  |
| 4 | `Type` | Type | Int | 6 | - |  | `1` = Page header<br>`2` = Start of report<br>`3` = Repetitive area header<br>`4` = Repetitive area<br>`5` = Repetitive area footer<br>`6` = End of report<br>`7` = Page footer<br>`10` = Text field<br>`11` = Picture field<br>`12` = User field |
| 5 | `VISIBLE` | Visible | VarChar | 1 | - | 1 | `1` = Yes<br>`0` = No |
| 6 | `SupZeros` | Suppress Zeros | VarChar | 1 | - | 0 | `1` = Yes<br>`0` = No |
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
| 20 | `BGRed` | Background - Red | Int | 11 | - | 65535 |  |
| 21 | `BGGreen` | Background - Green | Int | 11 | - | 65535 |  |
| 22 | `BGBlue` | Background - Blue | Int | 11 | - | 65535 |  |
| 23 | `FGRed` | Text - Red | Int | 11 | - | 0 |  |
| 24 | `FGGreen` | Text - Green | Int | 11 | - | 0 |  |
| 25 | `FGBlue` | Text - Blue | Int | 11 | - | 0 |  |
| 26 | `MrkrRed` | Bold - Red | Int | 11 | - | 65535 |  |
| 27 | `MrkrGreen` | Bold - Green | Int | 11 | - | 65535 |  |
| 28 | `MrkrBlue` | Bold - Blue | Int | 11 | - | 65535 |  |
| 29 | `BrdrRed` | Border - Red | Int | 11 | - | 0 |  |
| 30 | `BrdrGreen` | Border - Green | Int | 11 | - | 0 |  |
| 31 | `BrdrBlue` | Border - Blue | Int | 11 | - | 0 |  |
| 32 | `FromPane` | From Area | Int | 6 | - | 0 |  |
| 33 | `ToPane` | To Area | Int | 6 | - | 0 |  |
| 34 | `ItemGroup` | Group No. | Int | 6 | - | 0 |  |
| 35 | `FontName` | Font Name | nVarChar | 50 | - | Arial |  |
| 36 | `FontSize` | Font Size | Int | 6 | - | 12 |  |
| 37 | `TextStyle` | Text Style | Int | 11 | - |  |  |
| 38 | `Justific` | Horizontal Justification | VarChar | 1 | - | 2 | `1` = Right<br>`2` = Left<br>`3` = Center<br>`4` = Language Dependent |
| 39 | `WRAP` | Segment | VarChar | 1 | - | 1 | `0` = Allow overflow<br>`1` = Fit to cell<br>`2` = Devide to lines |
| 40 | `PictSize` | Picture Size | VarChar | 1 | - | 1 | `0` = Original size<br>`1` = Size of box<br>`2` = Adjust to box<br>`3` = Adjust to box height<br>`4` = Adjust to box width |
| 41 | `DataSource` | Data Source | VarChar | 1 | - | 1 | `1` = Static<br>`2` = Var<br>`3` = Data<br>`4` = Calculation |
| 42 | `ItemStr` | String | Text | 16 | - |  |  |
| 43 | `VarNum` | Variable No. | Int | 6 | - |  |  |
| 44 | `FileName` | File Name | nVarChar | 20 | - |  |  |
| 45 | `FieldNum` | Field No. | nVarChar | 10 | - |  |  |
| 46 | `ShowDescr` | Display Description | VarChar | 1 | - | 0 | `1` = Yes<br>`0` = No |
| 47 | `CalcType` | Calculation Type | nVarChar | 2 | - | 1 | `0` = Formula<br>`1` = Page number<br>`17` = Total Pages<br>`2` = Date<br>`3` = Time<br>`4` = Column total<br>`5` = Column average<br>`6` = General row no.<br>`7` = Group row no.<br>`8` = Sort field name<br>`9` = Sort field content<br>`10` = Continue<br>`11` = Continued on next page<br>`12` = Generation message<br>`13` = Column summary for page<br>`14` = Column average for page<br>`15` = Column summary for report<br>`16` = Column average for report<br>`-1` = [new formula String] |
| 48 | `ChangFlags` | Changeable | Int | 11 | - |  |  |
| 49 | `ApplID` | Item No. | Int | 6 | - |  |  |
| 50 | `CalcCol` | Calculation Column | Int | 6 | - |  |  |
| 51 | `YJustific` | Vertical Alignment | VarChar | 1 | - | 3 | `1` = Top<br>`2` = Bottom<br>`3` = Center |
| 52 | `SortLevel` | Sort Level | Int | 6 | - | 0 |  |
| 53 | `RevOrder` | Reverse Sort | VarChar | 1 | - | 0 | `1` = Descending<br>`0` = Ascending |
| 54 | `SortType` | Sort Type | VarChar | 1 | - | 0 | `0` = Alpha<br>`1` = Numeric<br>`2` = Money<br>`3` = Date |
| 55 | `IsUnique` | Unique | VarChar | 1 | - | 0 | `1` = Yes<br>`0` = No |
| 56 | `IsGroup` | Set as Group | VarChar | 1 | - | 0 | `1` = Yes<br>`0` = No |
| 57 | `NewPage` | New Page | VarChar | 1 | - | 0 | `1` = Yes<br>`0` = No |
| 58 | `BarCode` | Print as Barcode | VarChar | 1 | - | 0 | `1` = Yes<br>`0` = No |
| 59 | `Condition` | Condition | Text | 16 | - |  |  |
| 60 | `LinkTo` | Link to Item | Int | 6 | - | 0 |  |
| 61 | `Operator1` | Operator 1 | Int | 6 | - |  |  |
| 62 | `Operator2` | Operator 2 | Int | 6 | - |  |  |
| 63 | `Operation` | Operation | Int | 6 | - | 0 | `0`<br>`1` = +<br>`2` = -<br>`3` = x<br>`4` = /<br>`5` = %<br>`17` = Left<br>`18` = Right<br>`19` = Round<br>`6` = $Concat<br>`7` = $Right<br>`8` = $Left<br>`9` = $Sentence<br>`16` = $Len<br>`20` = $Currency<br>`21` = $Number<br>`10` = Less<br>`11` = LessEq<br>`12` = Equally<br>`13` = Not eq<br>`14` = GrEq<br>`15` = Greater |
| 64 | `BCStandard` | Barcode Standard | Int | 6 | - | 0 | `0` = EAN-13<br>`1` = Code 39<br>`2` = Code 128 |
| 65 | `SumInWords` | Display Total as a Word | VarChar | 1 | - | 0 | `1` = Yes<br>`0` = No |
| 66 | `ExcFonting` | Block Font Change | VarChar | 1 | - | 0 | `1` = Yes<br>`0` = No |
| 67 | `StrIndex` | String Index | Int | 11 | - | 0 |  |
| 68 | `ContIndex` | Container Index | Int | 6 | - | 0 |  |
| 69 | `ItemIndex` | Item Index | Int | 6 | - | 0 |  |
| 70 | `StrLength` | String Length | Int | 6 | - |  |  |
| 71 | `StrFiller` | String Filler | VarChar | 1 | - |  |  |
| 72 | `RelatedTo` | Related to Item | Int | 6 | - | 0 |  |
| 73 | `NextSeg` | Next Segment Item Num | Int | 6 | - | 0 |  |
| 74 | `HightAdjst` | Height Adjustments | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 75 | `DupRpttAre` | Duplicate Repeatative Area | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 76 | `LnsRpttAre` | Num Lines In Repeatative Area | Int | 11 | - | 0 |  |
| 77 | `RptDupDist` | Distanse To Rptt Dup (pixels) | Int | 11 | - | 0 |  |
| 78 | `ItemDesc` | Item Description | nVarChar | 50 | - |  |  |
| 79 | `ExportXml` | Export to xml | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 80 | `DocType` | Document Type | nVarChar | 4 | - |  |  |
| 81 | `Local` | Localization | nVarChar | 2 | - |  |  |
| 82 | `Numerator` | Numerator | Int | 6 | - |  |  |
| 83 | `Language` | Language | Int | 6 | - |  |  |
| 84 | `Created` | Creation Date | Date | 8 | - |  |  |
| 85 | `Updated` | Updated Date | Date | 8 | - |  |  |
| 86 | `UsrSgnStr` | User Sign For Strings Change | Int | 11 | - | -1 |  |
| 87 | `UsrSgnAttr` | User Sign For Attribs Change | Int | 11 | - | -1 |  |
| 88 | `IsRef` | Is the item refered by another | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 89 | `FieldId` | Field Identifier | nVarChar | 20 | - |  |  |
| 90 | `FGEnabled` | Grid Enabled | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 91 | `BGEnabled` | Background Enabled | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 92 | `MKEnabled` | Highlight Enabled | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 93 | `BDEnabled` | Frame Enabled | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 94 | `HidEmpRptt` | Hide Empty Area | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 95 | `RpttFtrAll` | Display Rep. Footer on All | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 96 | `GbiDataTyp` | Data Type | Int | 6 | - | 0 | `0`<br>`1` = C n<br>`2` = C.. n<br>`3` = I.. n<br>`4` = D w.d |
| 97 | `GbiDataLen` | Data Length | nVarChar | 6 | - |  |  |
| 98 | `PageBreak` | Page Break | Int | 6 | - | 0 | `0` = None<br>`1` = Before Area<br>`2` = After Area |
| 99 | `IsLogo` | Is Logo | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 100 | `VarDefName` | Variable Definition Name | nVarChar | 50 | - |  |  |
| 101 | `ResCode` | Resource Code from RSBD | Int | 11 | - | -1 |  |
| 102 | `RevCode` | Revision Code | Int | 11 | - | -1 |  |

## Claves e índices (5)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocType, Local, Numerator, Language, ApplID, ResCode, RevCode |
| TP_LC_NM_L | No | DocType, Local, Numerator, Language |
| TYP_LOC_NM | No | DocType, Local, Numerator |
| TYPE_LOC | No | DocType, Local |
| TYPE | No | DocType |
