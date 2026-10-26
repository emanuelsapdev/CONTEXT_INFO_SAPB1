# DOCR - DOCR

- **Tabla:** DOCR
- **Descripción:** DOCR
- **Cantidad de campos:** 60
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DOCR.html

## Campos (60)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocCode` | Code | nVarChar | 8 | - |  |  |
| 2 | `DocName` | Report Name | nVarChar | 64 | - |  |  |
| 3 | `Author` | Author | nVarChar | 32 | - |  |  |
| 4 | `Notes` | Remarks | nVarChar | 254 | - |  |  |
| 5 | `Width` | Width | Int | 6 | - | 595 |  |
| 6 | `Height` | Height | Int | 6 | - | 842 |  |
| 7 | `LMargin` | Left Margin | Int | 6 | - | 10 |  |
| 8 | `RMargin` | Right Margin | Int | 6 | - | 30 |  |
| 9 | `TMargin` | Top Margin | Int | 6 | - | 10 |  |
| 10 | `BMargin` | Bottom Margin | Int | 6 | - | 10 |  |
| 11 | `CanChange` | Changable | Int | 6 | - | 1 | `1` = TRUE<br>`0` = FALSE |
| 12 | `PaperSize` | Paper Size | nVarChar | 100 | - | A4 210 x 297 mm |  |
| 13 | `Oreint` | Orientation | VarChar | 1 | - | P | `P` = Vertical<br>`L` = Horizontal |
| 14 | `GridSize` | Grid Size | Int | 6 | - | 10 |  |
| 15 | `GridType` | Grid Type | VarChar | 1 | - | 1 | `1` = Compbination<br>`2` = Continuous line<br>`3` = Broken line<br>`4` = Dots |
| 16 | `ShowGrid` | Display Grid | VarChar | 1 | - | 1 | `1` = TRUE<br>`0` = FALSE |
| 17 | `SnapGrid` | Next to Grid | VarChar | 1 | - | 1 | `1` = TRUE<br>`0` = FALSE |
| 18 | `Picture` | Picture | Text | 16 | - |  |  |
| 19 | `TypeCode` | Type Code | nVarChar | 4 | - |  |  |
| 20 | `FrgnReport` | Foreign Language Report | VarChar | 1 | - | 0 | `1` = TRUE<br>`0` = FALSE |
| 21 | `CanSort` | Sortable | Int | 6 | - | 1 | `1` = TRUE<br>`0` = FALSE |
| 22 | `LeaderCode` | Leader Report | nVarChar | 8 | - |  |  |
| 23 | `FollowCode` | Follow-Up Report | nVarChar | 8 | - |  |  |
| 24 | `SwapOnScrn` | Convert Font in Print Preview | Int | 6 | - | 0 | `1` = Yes<br>`0` = FALSE |
| 25 | `ScreenFont` | Preview Printing Font | nVarChar | 50 | - | Arial |  |
| 26 | `ScrFOffset` | Change Font Size in Preview Pr | Int | 6 | - | -1 |  |
| 27 | `SwpInEmail` | Convert Font for E-mail | Int | 6 | - | 0 | `1` = Yes<br>`0` = FALSE |
| 28 | `EmailFont` | E-Mail Font | nVarChar | 50 | - | Arial |  |
| 29 | `EmFOffset` | Change Font Size for E-Mail | Int | 6 | - | -1 |  |
| 30 | `QString` | Query | Text | 16 | - |  |  |
| 31 | `QType` | Query Type | VarChar | 1 | - | R | `R` = Regular<br>`W` = Wizard |
| 32 | `Language` | Language | Int | 6 | - |  |  |
| 33 | `RobjCode` | Imp Exp Obj Code | Int | 11 | - | 0 |  |
| 34 | `ExtName` | Extension Name | Text | 16 | - |  |  |
| 35 | `ExtOnErr` | Action Taken On Ext Error | VarChar | 1 | - | S | `S` = Stop<br>`I` = Ignore<br>`P` = Promt |
| 36 | `NumRepArs` | Number of Repetitive Areas | Int | 6 | - | 1 |  |
| 37 | `AlgnFooter` | Allign Footer to Buttom | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 38 | `Local` | Localization | nVarChar | 2 | - |  |  |
| 39 | `Numerator` | Numerator | Int | 6 | - |  |  |
| 40 | `NextAppId` | Next Item AppId | Int | 6 | - | 1 |  |
| 41 | `Created` | Creation Date | Date | 8 | - |  |  |
| 42 | `Updated` | Updated Date | Date | 8 | - |  |  |
| 43 | `UsrSgnStr` | User Sign For Strings Change | Int | 11 | - | -1 |  |
| 44 | `UsrSgnAttr` | User Sign For Attribs Change | Int | 11 | - | -1 |  |
| 45 | `TimeFormat` | Time Template | VarChar | 1 | - | 0 | `0` = Default<br>`1` = 24H<br>`2` = 12H |
| 46 | `DateFormat` | Date Template | VarChar | 1 | - | 0 | `0` = Default<br>`1` = DD/MM/YY<br>`2` = DD/MM/CCYY<br>`3` = MM/DD/YY<br>`4` = MM/DD/CCYY<br>`5` = CCYY/MM/DD<br>`6` = DD/Month/YYYY |
| 47 | `DateSep` | Date Separator | VarChar | 1 | - |  |  |
| 48 | `DecSep` | Decimal Separator | VarChar | 1 | - |  |  |
| 49 | `ThousSep` | Thousands Separator | VarChar | 1 | - |  |  |
| 50 | `Printer` | Printer | nVarChar | 100 | - |  |  |
| 51 | `NumLayPage` | Number of Layout Pages | Int | 11 | - |  |  |
| 52 | `NumCopy` | Number of Copies | Int | 11 | - | 1 |  |
| 53 | `GbiSupport` | GBI settings supported | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 54 | `Use1stPrtr` | Use 1st page printer | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 55 | `Prtr1st` | Printer for First Page | nVarChar | 100 | - |  |  |
| 56 | `Shading` | Print item backgrounds | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 57 | `ForceExpXX` | Force Export XX Report | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 58 | `ResCode` | Resource Code from RSBD | Int | 11 | - | -1 |  |
| 59 | `RevCode` | Revision Code | Int | 11 | - | -1 |  |
| 60 | `UseSysPref` | Use System Preference | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (4)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | TypeCode, Local, Numerator, Language, ResCode, RevCode |
| TYP_LOC_NM | No | TypeCode, Local, Numerator |
| TYPE_LOC | No | TypeCode, Local |
| TYPE | No | TypeCode |
