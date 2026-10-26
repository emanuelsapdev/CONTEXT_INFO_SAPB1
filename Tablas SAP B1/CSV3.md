# CSV3 - A/R Correction Invoice Reversal - Freight

- **Tabla:** CSV3
- **Descripción:** A/R Correction Invoice Reversal - Freight
- **Cantidad de campos:** 81
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CSV3.html

## Campos (81)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [OCSV](OCSV.md) |  |  |
| 2 | `ExpnsCode` | Expense Code | Int | 11 | [OEXD](OEXD.md) |  |  |
| 3 | `LineTotal` | Total | Num | 19.6 | - |  |  |
| 4 | `TotalFrgn` | Total (FC) | Num | 19.6 | - |  |  |
| 5 | `TotalSumSy` | Total (SC) | Num | 19.6 | - |  |  |
| 6 | `PaidToDate` | Paid to Date | Num | 19.6 | - |  |  |
| 7 | `PaidFC` | Paid in FC | Num | 19.6 | - |  |  |
| 8 | `PaidSys` | Paid in SC | Num | 19.6 | - |  |  |
| 9 | `Comments` | Remarks | nVarChar | 100 | - |  |  |
| 10 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 166 |  |
| 11 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 12 | `DistrbMthd` | Distribution Method | VarChar | 1 | - |  | `N` = None<br>`Q` = Quantity<br>`V` = Volume<br>`W` = Weight<br>`E` = Equally<br>`T` = Row Total |
| 13 | `TaxStatus` | Tax Liable | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 14 | `VatGroup` | Tax Group | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 15 | `VatPrcnt` | Row Tax % | Num | 19.6 | - |  |  |
| 16 | `VatSum` | Tax Amount | Num | 19.6 | - |  |  |
| 17 | `VatSumFrgn` | Tax Amount (FC) | Num | 19.6 | - |  |  |
| 18 | `VatSumSy` | Tax Amount (SC) | Num | 19.6 | - |  |  |
| 19 | `DedVatSum` | Deductible Tax Amount | Num | 19.6 | - |  |  |
| 20 | `DedVatSumF` | Deductible Tax Amount (FC) | Num | 19.6 | - |  |  |
| 21 | `DedVatSumS` | Deductible Tax Amount (SC) | Num | 19.6 | - |  |  |
| 22 | `IsAcquistn` | Aquisition Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 23 | `TaxCode` | Tax Code | nVarChar | 8 | [OSTC](OSTC.md) |  |  |
| 24 | `TaxType` | Tax Type | VarChar | 1 | - | Y | `Y` = Regular Tax<br>`N` = No Tax<br>`U` = Use Tax |
| 25 | `WTLiable` | WT Liable | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 26 | `VatApplied` | Vat Applied | Num | 19.6 | - |  |  |
| 27 | `VatAppldFC` | Applied Tax (FC) | Num | 19.6 | - |  |  |
| 28 | `VatAppldSC` | Applied Tax (SC) | Num | 19.6 | - |  |  |
| 29 | `EquVatPer` | Equalization Tax % | Num | 19.6 | - |  |  |
| 30 | `EquVatSum` | Total Equalization Tax | Num | 19.6 | - |  |  |
| 31 | `EquVatSumF` | Total Equalization Tax (FC) | Num | 19.6 | - |  |  |
| 32 | `EquVatSumS` | Total Equalization Tax (SC) | Num | 19.6 | - |  |  |
| 33 | `LineVat` | Net Tax Amount | Num | 19.6 | - |  |  |
| 34 | `LineVatF` | Net Tax Amount (FC) | Num | 19.6 | - |  |  |
| 35 | `LineVatS` | Net Tax Amount (SC) | Num | 19.6 | - |  |  |
| 36 | `BaseMethod` | Base Method | VarChar | 1 | - |  | `N` = None<br>`Q` = Quantity<br>`V` = Volume<br>`W` = Weight<br>`T` = Total<br>`A` = All |
| 37 | `Stock` | Stock | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 38 | `LstPchPrce` | Last Purchase Price | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 39 | `AnalysRpt` | Analysis Report | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 40 | `BaseAbsEnt` | Base Abs Entry | Int | 11 | - | -1 |  |
| 41 | `BaseType` | Base Document Type | Int | 11 | - |  | `-1`<br>`0`<br>`165` = A/R Correction Invoice |
| 42 | `BaseRef` | Base Document Reference | Int | 11 | - |  |  |
| 43 | `BaseLnNum` | Base Document Line No. | Int | 11 | - |  |  |
| 44 | `LineNum` | line num | Int | 11 | - | -1 |  |
| 45 | `Status` | Status | VarChar | 1 | - | O | `O` = Open<br>`C` = Closed |
| 46 | `TrgType` | Target Type | Int | 11 | - |  |  |
| 47 | `TrgAbsEnt` | Target Abs. Entry | Int | 11 | - | -1 |  |
| 48 | `StDstr` | Stock Distributed Sum | Num | 19.6 | - |  |  |
| 49 | `StDstrSC` | Stock Distributed Sum (SC) | Num | 19.6 | - |  |  |
| 50 | `StDstrFC` | Stock Distributed Sum (FC) | Num | 19.6 | - |  |  |
| 51 | `FixCurr` | Fixation Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 52 | `VatDscntPr` | Tax Discount % | Num | 19.6 | - |  |  |
| 53 | `OcrCode` | Distribution Rule | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 54 | `TaxDistMtd` | Tax Distribution Method | VarChar | 1 | - |  | `N` = None<br>`Q` = Quantity<br>`V` = Volume<br>`W` = Weight<br>`E` = Equally<br>`T` = Row Total |
| 55 | `OcrCode2` | Distribution Rule2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 56 | `OcrCode3` | Distribution Rule3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 57 | `OcrCode4` | Distribution Rule4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 58 | `OcrCode5` | Distribution Rule5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 59 | `Project` | Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 60 | `VatGrpSrc` | VAT Group Source | VarChar | 1 | - | N | `N` = Not Defined<br>`M` = Manually Entered<br>`D` = Determined |
| 61 | `DrawnTotal` | Drawn Total | Num | 19.6 | - |  |  |
| 62 | `DrawnFC` | Drawn Total (FC) | Num | 19.6 | - |  |  |
| 63 | `DrawnSC` | Drawn Total (SC) | Num | 19.6 | - |  |  |
| 64 | `GrsAmount` | Gross Amount | Num | 19.6 | - |  |  |
| 65 | `GrsFC` | Gross Amount (FC) | Num | 19.6 | - |  |  |
| 66 | `GrsSC` | Gross Amount (SC) | Num | 19.6 | - |  |  |
| 67 | `BaseTotal` | Base Total for Calculation | VarChar | 1 | - | N | `N` = Net Total<br>`G` = Gross Total |
| 68 | `RetReqLC` | Return Request Amount | Num | 19.6 | - |  |  |
| 69 | `RetReqFC` | Return Request Amount (FC) | Num | 19.6 | - |  |  |
| 70 | `RetReqSC` | Return Request Amount (SC) | Num | 19.6 | - |  |  |
| 71 | `RRVatLC` | Return Request VAT Amount | Num | 19.6 | - |  |  |
| 72 | `RRVatFC` | Return Request VAT Amount (FC) | Num | 19.6 | - |  |  |
| 73 | `RRVatSC` | Return Request VAT Amount (SC) | Num | 19.6 | - |  |  |
| 74 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 75 | `ExtTaxRate` | External Tax Rate | Num | 19.6 | - |  |  |
| 76 | `ExtTaxSum` | External Tax Amount | Num | 19.6 | - |  |  |
| 77 | `TaxAmtSrc` | Tax Amount Source | VarChar | 1 | - | S | `S` = Internal System Calculation<br>`E` = External Calculation |
| 78 | `ExtTaxSumF` | External Tax Amount (FC) | Num | 19.6 | - |  |  |
| 79 | `ExtTaxSumS` | External Tax Amount (SC) | Num | 19.6 | - |  |  |
| 80 | `CUSplit` | CU Split | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 81 | `DocFreight` | Included in Operating Profit | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum |
| DOCUMENT | No | DocEntry, BaseAbsEnt |
