# OVTR - Tax Report

- **Tabla:** OVTR
- **Descripción:** Tax Report
- **Cantidad de campos:** 89
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OVTR.html

## Campos (89)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Abs Entry (Numerator) | Int | 11 | - |  |  |
| 2 | `ReportName` | Report Name | nVarChar | 50 | - |  |  |
| 3 | `RptLayout` | Report Layout | VarChar | 1 | - | R | `R` = Tax Register Book<br>`D` = Tax Declaration<br>`B` = Black List Country - Tax Declaration<br>`L` = Black List Country - Tax Declaration 2013<br>`A` = VAT Annual List<br>`I` = Annual Invoice Declaration 2011<br>`N` = Annual Invoice Declaration 2013<br>`P` = Declaration of Purchases from San Marino<br>`E` = Electronic Tax Declaration<br>`F` = Electronic Tax Declaration 2018<br>`M` = VAT Invoice Declaration 2017<br>`G` = Electronic Tax Declaration 2019<br>`T` = One-Stop Shop Declaration |
| 4 | `FirstPrint` | First Printed No. | Int | 11 | - |  |  |
| 5 | `FromDate` | Date From | Date | 8 | - |  |  |
| 6 | `ToDate` | Date To | Date | 8 | - |  |  |
| 7 | `TaxDate` | Document Date | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 8 | `RoundSum` | Round Amounts | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes<br>. |
| 9 | `Declration` | Declaration Type | VarChar | 1 | - | O | `O` = Original<br>`S` = Substitute<br>`C` = Complementary |
| 10 | `FilterType` | Selection Criteria Type | VarChar | 1 | - | N | `V` = Tax Report<br>`W` = Withholding Tax Report<br>`T` = Report 347<br>`E` = 349 Report<br>`R` = Reconciliation Report<br>`S` = Stamp Tax<br>`U` = Sales Report<br>`N` = None<br>`B` = Box Report<br>`O` = Appendix O or P Selection<br>`A` = Annual Sales Report<br>`F` = VAT Refund Report<br>`C` = Input/Output VAT Report |
| 11 | `ExcludeWT` | Exclude Withholding Tax | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 12 | `CustomerIn` | Include Customers | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 13 | `VendorIn` | Include Vendors | VarChar | 1 | - | Y | `N` = No<br>`Y` = Yes |
| 14 | `Period` | Quarter, Year or Month | VarChar | 1 | - | Q | `Q` = Quarter<br>`Y` = Year<br>`M` = Month<br>`S` = . |
| 15 | `Quarter` | Quarter | Int | 11 | - |  |  |
| 16 | `Year` | Year | Int | 11 | - |  |  |
| 17 | `DocType` | A/P or A/R | VarChar | 1 | - | P | `P` = Purchasing Documents<br>`R` = Sales Documents |
| 18 | `CreditMemo` | Credit Memos | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 19 | `DocTypeIn` | Include Document Type | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 20 | `FirstReg` | First Register Number | Int | 11 | - |  |  |
| 21 | `AccountIn` | Include G/L Accounts | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 22 | `DeferTaxIn` | Show Pmts with Deferred Tax | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 23 | `ApndxOOrP` | Appendix O or P Selection | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 24 | `DispOBCB` | Opening & Closing Balance | VarChar | 1 | - | Y | `N` = No<br>`Y` = Yes |
| 25 | `FromSeries` | From Tax Series Group | Int | 11 | - |  |  |
| 26 | `ToSeries` | To Tax Series Group | Int | 11 | - |  |  |
| 27 | `canceltn` | For EU Sales Report | VarChar | 1 | - | N |  |
| 28 | `HideNTrans` | Hide Tax Codes with no Trans. | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 29 | `SeriesIn` | Include Series Filter | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 30 | `UserCode` | User Code | nVarChar | 25 | - |  |  |
| 31 | `FromCardCo` | BP Code From | nVarChar | 15 | - |  |  |
| 32 | `ToCardCo` | BP Code To | nVarChar | 15 | - |  |  |
| 33 | `SizeOfStru` | Size of Structure | Int | 11 | - |  |  |
| 34 | `PostFrDate` | Posting Date From | Date | 8 | - |  |  |
| 35 | `PostToDate` | Posting Date To | Date | 8 | - |  |  |
| 36 | `DocFrDate` | Document Date From | Date | 8 | - |  |  |
| 37 | `DocToDate` | Document Date To | Date | 8 | - |  |  |
| 38 | `FromDoc1Nu` | Document 1 - From | nVarChar | 11 | - |  |  |
| 39 | `ToDoc1Nu` | Document 1 - To | nVarChar | 11 | - |  |  |
| 40 | `Serie1` | Invoice Numbering Series | nVarChar | 11 | - | Y | `Y` = Yes<br>`N` = No |
| 41 | `Serie1CB` | Inv. Numbering Series Filter | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 42 | `Doc1Type` | Type of Document 1 | Int | 11 | - |  |  |
| 43 | `FromDoc2Nu` | Document 2 - From | nVarChar | 11 | - |  |  |
| 44 | `ToDoc2Nu` | Document 2 - To | nVarChar | 11 | - |  |  |
| 45 | `Serie2` | Credit Memo Numbering Series | nVarChar | 11 | - | Y | `Y` = Yes<br>`N` = No |
| 46 | `Serie2CB` | Corr. Inv. Rev. No. Series | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 47 | `Doc2Type` | Type of Document 2 | Int | 11 | - |  |  |
| 48 | `FromDoc3Nu` | Document 3 - From | nVarChar | 11 | - |  |  |
| 49 | `ToDoc3Nu` | Document 3 - To | nVarChar | 11 | - |  |  |
| 50 | `Serie3` | Corr. Inv. Numbering Series | nVarChar | 11 | - | Y | `Y` = Yes<br>`N` = No |
| 51 | `Serie3CB` | Corr. Inv. Num. Series Filter | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 52 | `Doc3Type` | Type of Document 3 | Int | 11 | - |  |  |
| 53 | `FromDoc4Nu` | Document 4 - From | nVarChar | 11 | - |  |  |
| 54 | `ToDoc4Nu` | Document 4 - To | nVarChar | 11 | - |  |  |
| 55 | `Serie4` | Corr. Inv. Rev. No. Series | nVarChar | 11 | - | Y | `Y` = Yes<br>`N` = No |
| 56 | `Serie4CB` | Corr. Inv. Reversal No. Series | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 57 | `Doc4Type` | Type of Document 4 | Int | 11 | - |  |  |
| 58 | `FromDoc5Nu` | Document 5 - From | nVarChar | 11 | - |  |  |
| 59 | `ToDoc5Nu` | Document 5 - To | nVarChar | 11 | - |  |  |
| 60 | `Serie5` | Down Payment Numbering Series | nVarChar | 11 | - | Y | `Y` = Yes<br>`N` = No |
| 61 | `Serie5CB` | Down Payment Numbering Series | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 62 | `Doc5Type` | Type of Document 5 | Int | 11 | - |  |  |
| 63 | `DateRBtn` | Report Period | VarChar | 1 | - | I | `I` = Interval<br>`D` = Date |
| 64 | `MarkDocsIn` | Include Marketing Documents | VarChar | 1 | - | Y | `N` = No<br>`Y` = Yes |
| 65 | `ExRate` | Exchange Rate | VarChar | 1 | - | P | `P` = Posting<br>`R` = For Reports |
| 66 | `ExRateDate` | Exchange Rate Date | VarChar | 1 | - | P | `P` = Posting Date<br>`D` = Document Date<br>`V` = VAT Date |
| 67 | `TrsPerioTp` | Report Period Type | VarChar | 1 | - |  | `Y` = Year<br>`Q` = Quarter<br>`B` = Bi-Monthly<br>`M` = Month<br>`P` = Period<br>`F` = Fiscal Year<br>`G` = Fiscal Quarter |
| 68 | `TrsPerioNu` | Report Period Number | Int | 11 | - |  |  |
| 69 | `TrsYear` | Report Year | Int | 6 | - |  |  |
| 70 | `TrsAdjtNum` | Report Adjustment Number | Int | 6 | - |  |  |
| 71 | `DateType` | Date Type | VarChar | 1 | - | P | `P` = Posting Date<br>`D` = Document Date<br>`V` = VAT Date<br>`C` = System Date |
| 72 | `IncServDoc` | Include Service Documents | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 73 | `GrpBySCode` | Group by Sales Code | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 74 | `IncUnReDoc` | Include Unreconciled Documents | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 75 | `DoYearSum` | Year Summary | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 76 | `DefTaxOnly` | Only Include Deferred Tax Docs | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 77 | `ExcElDoc` | Exclude Electronic Documents | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 78 | `QtrByMnt` | Quarter by Months | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 79 | `OnlyExtnTx` | Only External Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 80 | `IncludeWTR` | Include Inventory Transfers | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 81 | `FromMark` | MARK From | nVarChar | 40 | - |  |  |
| 82 | `ToMark` | MARK To | nVarChar | 40 | - |  |  |
| 83 | `IsueFrDate` | Issue Date From | Date | 8 | - |  |  |
| 84 | `IsueToDate` | Issue Date To | Date | 8 | - |  |  |
| 85 | `FromVatNo` | Issuer VAT No. From | nVarChar | 64 | - |  |  |
| 86 | `ToVatNo` | Issuer VAT No. To | nVarChar | 64 | - |  |  |
| 87 | `FrInvType` | Invoice Type From | nVarChar | 50 | - |  |  |
| 88 | `ToInvType` | Invoice Type To | nVarChar | 50 | - |  |  |
| 89 | `IncludeDpm` | Include Down Payment | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| NAME | Yes | ReportName, FilterType |
