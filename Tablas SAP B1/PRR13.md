# PRR13 - A/P Return Request - Distributed Freights

- **Tabla:** PRR13
- **Descripción:** A/P Return Request - Distributed Freights
- **Cantidad de campos:** 60
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PRR13.html

## Campos (60)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [OPRR](OPRR.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `GroupNum` | Group Number | Int | 11 | - |  |  |
| 4 | `ExpnsCode` | Freight Code | Int | 11 | [OEXD](OEXD.md) |  |  |
| 5 | `LineTotal` | Total | Num | 19.6 | - |  |  |
| 6 | `TotalFrgn` | Total (FC) | Num | 19.6 | - |  |  |
| 7 | `TotalSumSy` | Total (SC) | Num | 19.6 | - |  |  |
| 8 | `PaidToDate` | Paid to Date | Num | 19.6 | - |  |  |
| 9 | `PaidFC` | Paid (FC) | Num | 19.6 | - |  |  |
| 10 | `PaidSys` | Paid (SC) | Num | 19.6 | - |  |  |
| 11 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 234000032 |  |
| 12 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
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
| 24 | `TaxType` | Tax Type | VarChar | 1 | - | Y | `Y` = Normal Tax<br>`N` = No Tax<br>`U` = Use Tax |
| 25 | `VatApplied` | VAT Applied | Num | 19.6 | - |  |  |
| 26 | `VatAppldFC` | VAT Applied Frgn | Num | 19.6 | - |  |  |
| 27 | `VatAppldSC` | VAT Applied Sys | Num | 19.6 | - |  |  |
| 28 | `EquVatPer` | Equalization Tax % | Num | 19.6 | - |  |  |
| 29 | `EquVatSum` | Total Equalization Tax | Num | 19.6 | - |  |  |
| 30 | `EquVatSumF` | Total Equalization Tax (FC) | Num | 19.6 | - |  |  |
| 31 | `EquVatSumS` | Total Equalization Tax (SC) | Num | 19.6 | - |  |  |
| 32 | `lineVat` | Net Tax Amount | Num | 19.6 | - |  |  |
| 33 | `lineVatlF` | Net Tax Amount (FC) | Num | 19.6 | - |  |  |
| 34 | `lineVatS` | Net Tax Amount (SC) | Num | 19.6 | - |  |  |
| 35 | `WtLiable` | WTax Liable | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 36 | `BaseMethod` | Base Method | VarChar | 1 | - |  | `N` = None<br>`Q` = Quantity<br>`V` = Volume<br>`W` = Weight<br>`T` = Total<br>`A` = All |
| 37 | `Stock` | Stock | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 38 | `LstPchPrce` | Last Purchase Price | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 39 | `AnalysRpt` | Analysis Report | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 40 | `BaseAbsEnt` | Base Abs Entry | Int | 11 | - | -1 |  |
| 41 | `BaseType` | Base Document Type | Int | 11 | - |  |  |
| 42 | `BaseRef` | Base Document Reference | Int | 11 | - |  |  |
| 43 | `BaseLnNum` | Base Document Line No. | Int | 11 | - |  |  |
| 44 | `TrgType` | Target Type | Int | 11 | - |  |  |
| 45 | `TrgAbsEnt` | Target Abs. Entry | Int | 11 | - | -1 |  |
| 46 | `BaseGroup` | Base Document Group | Int | 11 | - | -1 |  |
| 47 | `Status` | Status | VarChar | 1 | - | O | `O` = Open<br>`C` = Close |
| 48 | `TrgGroup` | Target Group | Int | 11 | - | -1 |  |
| 49 | `VisOrder` | Visual Order | Int | 11 | - |  |  |
| 50 | `DistrbMthd` | Distribution Method | VarChar | 1 | - |  | `N` = None<br>`Q` = Quantity<br>`V` = Volume<br>`W` = Weight<br>`E` = Equally<br>`T` = Row Total |
| 51 | `DistribExp` | Distribute Freights | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 52 | `FixCurr` | Fixation Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 53 | `VatDscntPr` | Tax Discount % | Num | 19.6 | - |  |  |
| 54 | `OcrCode` | Distribution Rule | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 55 | `OcrCode2` | Distribution Rule2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 56 | `OcrCode3` | Distribution Rule3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 57 | `OcrCode4` | Distribution Rule4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 58 | `OcrCode5` | Distribution Rule5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 59 | `Project` | Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 60 | `DocFreight` | Included in Operating Profit | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum, GroupNum |
| LINE | No | DocEntry, LineNum |
