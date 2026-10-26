# OUDG - User Defaults

- **Tabla:** OUDG
- **Descripción:** User Defaults
- **Cantidad de campos:** 50
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OUDG.html

## Campos (50)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | nVarChar | 8 | - |  |  |
| 2 | `Name` | Name | nVarChar | 20 | - |  |  |
| 3 | `Warehouse` | Warehouse | nVarChar | 8 | [OWHS](OWHS.md) |  |  |
| 4 | `SalePerson` | Sales Employee | Int | 11 | [OSLP](OSLP.md) | -1 |  |
| 5 | `ICTCard` | BP for Invoice + Payment | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 6 | `CashAcct` | Cash Account | nVarChar | 15 | - |  |  |
| 7 | `CheckAcct` | Current Account | nVarChar | 15 | - |  |  |
| 8 | `CreditCard` | Credit Card | Int | 6 | [OCRC](OCRC.md) |  |  |
| 9 | `PrintRcpt` | Print Receipt | VarChar | 1 | - | N | `N` = No<br>`A` = Only When Adding<br>`Y` = Always |
| 10 | `ShortRcpt` | Print Payment & Invoice in Succession | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 11 | `Color` | Windows Color | Int | 6 | - |  | `0` = Combined<br>`1` = Classic<br>`2` = Gray<br>`3` = Violet<br>`4` = Blue<br>`5` = Green<br>`6` = Yellow<br>`7` = Orange<br>`8` = Red<br>`9` = Brown |
| 12 | `Address` | Address | nVarChar | 254 | - |  |  |
| 13 | `Country` | Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 14 | `PrintHeadr` | Printing Header | nVarChar | 100 | - |  |  |
| 15 | `Phone1` | Telephone Number 1 | nVarChar | 50 | - |  |  |
| 16 | `Phone2` | Telephone Number 2 | nVarChar | 50 | - |  |  |
| 17 | `Fax` | Fax Number | nVarChar | 50 | - |  |  |
| 18 | `E_Mail` | E-Mail | nVarChar | 100 | - |  |  |
| 19 | `FrgnAddr` | Address in Foreign Language | nVarChar | 254 | - |  |  |
| 20 | `FrnPrntHdr` | Printing Header in Foreign Lan | nVarChar | 100 | - |  |  |
| 21 | `FrgnPhone1` | Telephone Number 1 (Foreign Lang.) | nVarChar | 50 | - |  |  |
| 22 | `FrgnPhone2` | Telephone Number 2 (Foreign Lang.) | nVarChar | 50 | - |  |  |
| 23 | `FrgnFax` | Fax Number (Foreign Lang.) | nVarChar | 50 | - |  |  |
| 24 | `DflTaxCode` | Default Tax Code | nVarChar | 8 | [OSTC](OSTC.md) |  |  |
| 25 | `FreeZoneNo` | Additional ID Number | nVarChar | 32 | - |  |  |
| 26 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 27 | `free1` | Free1 | VarChar | 1 | - |  |  |
| 28 | `UseTax` | Use Tax | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 29 | `AdrsFromWh` | Use Warehouse Address in A/P Documents | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 30 | `Language` | Language | Int | 11 | [OLNG](OLNG.md) |  |  |
| 31 | `Font` | Font | nVarChar | 50 | - |  |  |
| 32 | `FontSize` | Font Size | Int | 11 | - |  |  |
| 33 | `BPLId` | Default Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 34 | `AssetInDoc` | Allow Creation of Asset in Doc. | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 35 | `AttachPath` | Attachments Path | Text | 16 | - |  |  |
| 36 | `DflPTICode` | Default POI Code | nVarChar | 5 | [OPTI](OPTI.md) |  |  |
| 37 | `Free4` | unused | VarChar | 1 | - |  |  |
| 38 | `Free2` | unused | VarChar | 1 | - |  |  |
| 39 | `Free3` | unused | VarChar | 1 | - |  |  |
| 40 | `DflPosCR` | Default POS/Cash Register | Int | 11 | [OPCM](OPCM.md) |  |  |
| 41 | `TimeFormat` | Time Template | VarChar | 1 | - |  | `0` = 24H<br>`1` = 12H |
| 42 | `DateFormat` | Date Template | VarChar | 1 | - |  | `0` = DD/MM/YY<br>`1` = DD/MM/YYYY<br>`2` = MM/DD/YY<br>`3` = MM/DD/YYYY<br>`4` = CCYY/MM/DD<br>`5` = DD/Month/YYYY<br>`6` = YY/MM/DD |
| 43 | `DateSep` | Date Separator | VarChar | 1 | - |  |  |
| 44 | `DecSep` | Decimal Separator | VarChar | 1 | - |  |  |
| 45 | `ThousSep` | Thousands Separator | VarChar | 1 | - |  |  |
| 46 | `WallPaper` | Wallpaper | Text | 16 | - |  |  |
| 47 | `WllPprDsp` | Wallpaper Display | nVarChar | 6 | - |  | `1` = Centralized<br>`2` = Full Screen<br>`3` = Tile |
| 48 | `SkinType` | Skin Type | nVarChar | 254 | - |  |  |
| 49 | `CharMonth` | Number of Characters in Month | Int | 11 | - |  |  |
| 50 | `HandleEDoc` | Can Take Control of eDoc Processing in Electronic Document Monitor | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
