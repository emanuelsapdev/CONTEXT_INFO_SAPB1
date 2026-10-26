# OISW - Intrastat Wizard

- **Tabla:** OISW
- **Descripción:** Intrastat Wizard
- **Cantidad de campos:** 73
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OISW.html

## Campos (73)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Key | Int | 11 | - |  |  |
| 2 | `DeclDescr` | Description | nVarChar | 200 | - |  |  |
| 3 | `DateFrom` | Starting Date of Declaration | Date | 8 | - |  |  |
| 4 | `DateTo` | Ending Date of Declaration | Date | 8 | - |  |  |
| 5 | `RunDate` | Date of Run | Date | 8 | - |  |  |
| 6 | `ImpExpInd` | Import Export Indicator | VarChar | 1 | - | I | `I` = Import<br>`E` = Export |
| 7 | `Status` | Status | VarChar | 1 | - |  | `O` = Open<br>`C` = Closed<br>`D` = Deleted<br>`A` = Archived |
| 8 | `MsgType` | Message Type | Int | 11 | - | 0 | `0` = New Declaration<br>`9` = Nil Declaration<br>`3` = Correction Declaration |
| 9 | `TtlDocVal` | Total Document Value | Num | 19.6 | - |  |  |
| 10 | `DocCount` | Total Number of Documents | Int | 11 | - |  |  |
| 11 | `CompName` | Company Name | nVarChar | 200 | - |  |  |
| 12 | `CompDeclID` | Company Declaration ID | nVarChar | 32 | - |  |  |
| 13 | `CompStreet` | Company Street | nVarChar | 100 | - |  |  |
| 14 | `CompCity` | Company City | nVarChar | 100 | - |  |  |
| 15 | `CompZip` | Company Zip Code | nVarChar | 20 | - |  |  |
| 16 | `CompCntry` | Company Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 17 | `DeclCntry` | Declaration Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 18 | `CntPersID` | Contact Person ID | Int | 11 | [OHEM](OHEM.md) |  |  |
| 19 | `CntPerson` | Contact Person | nVarChar | 250 | - |  |  |
| 20 | `CntEmail` | Contact E-Mail | nVarChar | 100 | - |  |  |
| 21 | `CntPhone` | Contact Phone | nVarChar | 50 | - |  |  |
| 22 | `CntFax` | Contact Fax | nVarChar | 50 | - |  |  |
| 23 | `VATRegNo` | VAT Reg. No. of Trader | nVarChar | 100 | - |  |  |
| 24 | `VATRegEx` | VAT Reg. No. Extension | nVarChar | 10 | - |  |  |
| 25 | `DeclNum` | Sequential Declaration Number | nVarChar | 14 | - |  |  |
| 26 | `DeclNoEx` | No. of Declaration in Period | Int | 11 | - |  |  |
| 27 | `HeaderId` | Header ID | Int | 11 | - |  |  |
| 28 | `DeclStat` | Declaration Status | VarChar | 1 | - |  |  |
| 29 | `DeclDept` | Declaring Department | Int | 6 | - |  |  |
| 30 | `DeclCurr` | Declaration Currency | nVarChar | 3 | - |  |  |
| 31 | `ObligLvl` | Degree of Obligation | VarChar | 1 | - |  |  |
| 32 | `TaxState` | Federal State of Tax Office | nVarChar | 3 | - |  |  |
| 33 | `CustOffc` | Customs Registration Office | nVarChar | 100 | - |  |  |
| 34 | `CustOffID` | Customs Registration Office ID | nVarChar | 2 | - |  |  |
| 35 | `DeclSerNo` | Declaration Sequence Number | nVarChar | 3 | - |  |  |
| 36 | `IntCtrlRef` | Interchange Control Reference | nVarChar | 99 | - |  |  |
| 37 | `Addr1_3p` | Third-Party Address Part 1 | nVarChar | 100 | - |  |  |
| 38 | `Addr2_3p` | Third-Party Address Part 2 | nVarChar | 100 | - |  |  |
| 39 | `Addr3_3p` | Third-Party Address Part 3 | nVarChar | 100 | - |  |  |
| 40 | `Addr4_3p` | Third-Party Address Part 4 | nVarChar | 100 | - |  |  |
| 41 | `CntPers_3p` | Third-Party Contact Person | nVarChar | 250 | - |  |  |
| 42 | `CntPhon_3p` | Third-Party Contact Phone | nVarChar | 20 | - |  |  |
| 43 | `CntFax_3p` | Third-Party Contact Fax | nVarChar | 20 | - |  |  |
| 44 | `FreeTxt1` | Free Text Line 1 | nVarChar | 70 | - |  |  |
| 45 | `FreeTxt2` | Free Text Line 2 | nVarChar | 70 | - |  |  |
| 46 | `FreeTxt3` | Free Text Line 3 | nVarChar | 70 | - |  |  |
| 47 | `FreeTxt4` | Free Text Line 4 | nVarChar | 70 | - |  |  |
| 48 | `FreeTxt5` | Free Text Line 5 | nVarChar | 70 | - |  |  |
| 49 | `ValidKey` | Validation Key Identification | nVarChar | 35 | - |  |  |
| 50 | `ISDeclOffc` | Intrastat Declaration Office | nVarChar | 10 | - |  |  |
| 51 | `ReleaseVer` | Release Version | nVarChar | 13 | - |  |  |
| 52 | `UserSign` | Created by User | Int | 6 | - |  |  |
| 53 | `PosCredVal` | Positive Credit Memo Values | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 54 | `IncPrevDoc` | Include Previous Documents | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 55 | `DeclPeriod` | Declaration Period | VarChar | 1 | - | M | `M` = Monthly<br>`Q` = Quarterly |
| 56 | `Box1` | Box 1: Periodicity | Int | 6 | - | 0 | `0` = None of the Other Cases<br>`8` = First Month of Quarter<br>`9` = First and Second Months of Quarter |
| 57 | `Box2` | Box 2: Company Activity | Int | 6 | - | 0 | `0` = None of the Other Cases<br>`7` = First Declaration<br>`8` = Stop Activity/Change of Federal Tax ID<br>`9` = First Declaration After Federal Tax ID Change |
| 58 | `GroupData` | Group Display Data | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 59 | `CstRecSt` | Custom Section | nVarChar | 6 | - |  |  |
| 60 | `TaxCodeExt` | Tax Code Extension | nVarChar | 99 | - |  |  |
| 61 | `ExportPath` | Export Path | Text | 16 | - |  |  |
| 62 | `LLEFMAbs` | EFM Template ID | Int | 11 | - |  |  |
| 63 | `SimpProc` | Simplified Procedure | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 64 | `DspNMass` | Require All Data | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 65 | `ExlDocQt` | Exclude Docs W/ Qty Less Than | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 66 | `DocQtLm` | Document Quantity Limit | Num | 19.6 | - |  |  |
| 67 | `ExlDocAm` | Exclude Docs W/ Amt Less Than | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 68 | `DocAmLm` | Document Amount Limit | Num | 19.6 | - |  |  |
| 69 | `RunTime` | Time of Run | Int | 6 | - |  |  |
| 70 | `AddonRun` | Upgraded Add-On Run | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 71 | `BaseDecl` | Base Declaration | Int | 11 | [ODCI](ODCI.md) |  |  |
| 72 | `GroupTrans` | Group Transactions | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 73 | `IncGRandDL` | Include Goods Receipt and Deliveries | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
