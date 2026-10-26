# ADM2 - Administration Electronic Report

- **Tabla:** ADM2
- **Descripción:** Administration Electronic Report
- **Cantidad de campos:** 68
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ADM2.html

## Campos (68)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | Int | 11 | - |  |  |
| 2 | `TaxAuCod` | Tax Authority Code | nVarChar | 5 | - |  |  |
| 3 | `KeyEcoAct` | Key Economic Activity | nVarChar | 10 | - |  |  |
| 4 | `TaxPayType` | Tax Payer Type | VarChar | 1 | - | P | `P` = �94<br>`I` = �96<br>`S` = �95a |
| 5 | `TaxLegForm` | Tax Payer Legal Form | VarChar | 1 | - | P | `F` = Sole Proprietorship<br>`P` = Company |
| 6 | `RegName` | Registered Name | nVarChar | 254 | - |  |  |
| 7 | `RegNameExt` | Registered Name Extension | nVarChar | 11 | - |  |  |
| 8 | `SoleFName` | Sole Proprietor First Name | nVarChar | 20 | - |  |  |
| 9 | `SoleSName` | Sole Proprietor Surname | nVarChar | 36 | - |  |  |
| 10 | `SoleTitle` | Sole Proprietor Title | nVarChar | 10 | - |  |  |
| 11 | `CityTown` | City/Town/Village | nVarChar | 48 | - |  |  |
| 12 | `ZipCode` | Zip Code | nVarChar | 10 | - |  |  |
| 13 | `Telephone` | Telephone | nVarChar | 50 | - |  |  |
| 14 | `Street` | Street | nVarChar | 38 | - |  |  |
| 15 | `StreetNum` | Street Number | nVarChar | 4 | - |  |  |
| 16 | `BuildinNum` | Building Number | Int | 11 | - |  |  |
| 17 | `Email` | E-Mail | nVarChar | 254 | - |  |  |
| 18 | `State` | State | nVarChar | 20 | - |  |  |
| 19 | `RepType` | Representative Type | VarChar | 1 | - | P | `F` = Sole Proprietorship<br>`P` = Company |
| 20 | `RepCode` | Representative Code | nVarChar | 2 | - |  | `1` = Legal Representative<br>`2` = Authorized Representative<br>`3` = Common Representative, Contractual Representative<br>`4a` = General Appointee - Sole Proprietorship or Company<br>`4b` = Tax Advisor or Attorney<br>`4c` = Tax Advisor |
| 21 | `RepFName` | Representative First Name | nVarChar | 20 | - |  |  |
| 22 | `RepSName` | Representative Surname | nVarChar | 36 | - |  |  |
| 23 | `CompName` | Company Name | nVarChar | 36 | - |  |  |
| 24 | `BirthDate` | Birth Date | Date | 8 | - |  |  |
| 25 | `TaxACNum` | Tax Advisor Certificate Number | nVarChar | 36 | - |  |  |
| 26 | `LegEntitID` | Legal Entity ID | nVarChar | 10 | - |  |  |
| 27 | `AuthFName` | Authorized Person First Name | nVarChar | 20 | - |  |  |
| 28 | `AuthLName` | Authorized Person Last Name | nVarChar | 36 | - |  |  |
| 29 | `AuthRelat` | Authorized Person Relation | nVarChar | 40 | - |  |  |
| 30 | `AuthType` | Type of Authorized Person | VarChar | 1 | - |  |  |
| 31 | `TaxPayAttr` | Taxpayer Attribute | nVarChar | 2 | - |  |  |
| 32 | `Classifier` | Territorial/Adm. Classifier | nVarChar | 11 | - |  |  |
| 33 | `DeprMethod` | Depreciation Method | VarChar | 1 | - |  |  |
| 34 | `SubmitPlac` | Place of Submission | nVarChar | 3 | - |  |  |
| 35 | `BgtClass` | Budget Classification Code | nVarChar | 20 | - |  |  |
| 36 | `SubjOfRuF` | Subject of Russian Federation | nVarChar | 20 | - |  |  |
| 37 | `AuthFathrN` | Father Name | nVarChar | 254 | - |  |  |
| 38 | `BgtCleVAT` | Budget Classification Code (E-VAT) | nVarChar | 20 | - |  |  |
| 39 | `RepTitle` | Representative Title | nVarChar | 10 | - |  |  |
| 40 | `TaxRegime` | Tax Regime | nVarChar | 5 | - | RF01 | `RF01` = Ordinary<br>`RF02` = Minimum taxpayers (Art. 1, section 96-117, Italian Law 244/07)<br>`RF03` = New production initiatives (Art. 13, Italian Law 388/00)<br>`RF04` = Agriculture and connected activities, and fishing (Arts. 34 and 34-bis, Italian Presidential Decree 633/72)<br>`RF05` = Sale of salts and tobaccos (Art. 74, section 1, Italian Presidential Decree 633/72)<br>`RF06` = Match sales (Art. 74, section 1, Italian Presidential Decree 633/72)<br>`RF07` = Publishing (Art. 74, section 1, Italian Presidential Decree 633/72)<br>`RF08` = Management of public telephone services (Art. 74, section 1, Italian Presidential Decree 633/72)<br>`RF09` = Resale of public transport and parking documents (Art. 74, section 1, Italian Presidential Decree 633/72)<br>`RF10` = Entertainment, gaming and other activities referred to by the tariff attached to Italian Presidential Decree 640/72 (Art. 74, section 6, Italian Presidential Decree 633/1972)<br>`RF11` = Travel and tourism agencies (Art. 74-ter, Italian Presidential Decree 633/72)<br>`RF12` = Farmhouse accommodation/restaurants (Art. 5, section 2, Italian Law 413/91)<br>`RF13` = Door-to-door sales (Art. 25-bis, section 6, Italian Presidential Decree 600/73)<br>`RF14` = Resale of used goods, artworks, antiques or collector's items (Art. 36, Italian Decree Law 41/95)<br>`RF15` = Artwork, antiques or collector's items auction agencies (Art. 40-bis, Italian Decree Law 41/95)<br>`RF16` = VAT paid in cash by P.A. (Art. 6, section 5, Italian Presidential Decree 633/72)<br>`RF17` = VAT paid in cash by subjects with business turnover below Euro 200,000 (Art. 7, Italian Decree Law 185/2008)<br>`RF18` = Other<br>`RF19` = Regime forfettario (art.1, c.54-89, L. 190/2014)<br>`RF20` = Regime transfrontaliero di Franchigia IVA (Direttiva UE 2020/285) |
| 41 | `SoleBDate` | Sole Proprietor Date of Birth | Date | 8 | - |  |  |
| 42 | `SoleGender` | Sole Proprietor Gender | VarChar | 1 | - | M | `F` = Female<br>`M` = Male<br>`E` = Not Specified |
| 43 | `SoleCity` | Sole Proprietor City of Birth | nVarChar | 40 | - |  |  |
| 44 | `SoleDistri` | Sole Proprietor State of Birth | nVarChar | 3 | - |  |  |
| 45 | `RepFisCode` | Representative Fiscal Code | nVarChar | 16 | - |  |  |
| 46 | `RepPosCode` | Representative Position Code | nVarChar | 2 | - |  |  |
| 47 | `RepGender` | Representative Gender | VarChar | 1 | - | M | `F` = Female<br>`M` = Male<br>`E` = Not Specified |
| 48 | `RepCity` | Representative City of Birth | nVarChar | 40 | - |  |  |
| 49 | `RepDistri` | Representative State of Birth | nVarChar | 3 | - |  |  |
| 50 | `RepDate1` | Representative Start Date of Procedure | Date | 8 | - |  |  |
| 51 | `RepDate2` | Representative End Date of Procedure | Date | 8 | - |  |  |
| 52 | `RepPhone` | Representative Telephone | nVarChar | 14 | - |  |  |
| 53 | `RepEmail` | Representative E-Mail | nVarChar | 254 | - |  |  |
| 54 | `Country` | Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 55 | `District` | District | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 56 | `RegDistri` | Register District | nVarChar | 3 | - |  |  |
| 57 | `RegSCAmnt` | Share Capital Amount | Num | 19.6 | - |  |  |
| 58 | `RegSHolder` | Shareholder | nVarChar | 2 | - | SU | `SU` = Sole Shareholder<br>`SM` = Several Shareholders |
| 59 | `RegLiquida` | Liquidation | nVarChar | 2 | - | LN | `LS` = In Liquidation<br>`LN` = Not in Liquidation |
| 60 | `RepAddID` | Representative Additional ID | nVarChar | 28 | - |  |  |
| 61 | `ActCode` | Activity Code | nVarChar | 15 | - |  |  |
| 62 | `PosCode347` | Position Code for Report 347 | nVarChar | 2 | - |  | `1` = 1<br>`2` = 2<br>`3` = 3<br>`4` = 4<br>`5` = 5<br>`6` = 6<br>`7` = 7<br>`8` = 8<br>`9` = 9<br>`10` = 10<br>`11` = 11<br>`12` = 12<br>`13` = 13<br>`14` = 14<br>`15` = 15 |
| 63 | `FiscalCode` | Fiscal Code | nVarChar | 16 | - |  |  |
| 64 | `DataBoxID` | Data Box ID | nVarChar | 10 | - |  |  |
| 65 | `SmValLimit` | Small Value Documents Limit | Num | 19.6 | - |  |  |
| 66 | `RepCEOName` | Representative CEO Name | nVarChar | 254 | - |  |  |
| 67 | `RepCEOFisC` | Representative CEO Fiscal Code | nVarChar | 16 | - |  |  |
| 68 | `CmpnTypeFR` | Type d'entreprise | nVarChar | 30 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
