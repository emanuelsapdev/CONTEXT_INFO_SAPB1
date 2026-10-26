# UTX1 - Unreported VAT Transactions - Rows

- **Tabla:** UTX1
- **Descripción:** Unreported VAT Transactions - Rows
- **Cantidad de campos:** 103
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/UTX1.html

## Campos (103)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal ID | Int | 11 | [OUTX](OUTX.md) |  |  |
| 2 | `LineSeq` | Row Sequence | Int | 11 | - |  |  |
| 3 | `SrcArrType` | Source Array Type | Int | 11 | - | -1 | `-1` = Default<br>`1` = Main<br>`12` = Array1<br>`13` = Array2<br>`14` = Array3<br>`15` = Array4<br>`16` = Array5<br>`17` = Array6<br>`18` = Array7<br>`24` = Array13 |
| 4 | `SrcLineNum` | Source Row Number | Int | 11 | - | -1 |  |
| 5 | `SrcGrpNum` | Source Group Number | Int | 11 | - | -1 | `-1` = Default<br>`0` = Group1<br>`1` = Group2<br>`2` = Group3 |
| 6 | `TaxCode` | Tax Code | nVarChar | 8 | - |  |  |
| 7 | `StaCode` | Tax Authority Code | nVarChar | 8 | [OSTA](OSTA.md) |  |  |
| 8 | `StaType` | Tax Authority Type | Int | 11 | [OSTT](OSTT.md) |  |  |
| 9 | `StaIndex` | Tax Authority Seq Index | Int | 11 | - |  |  |
| 10 | `IsLiable` | Is Tax Liable | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 11 | `TaxType` | Tax Type | VarChar | 1 | - | Y | `Y` = Regular<br>`U` = Use Tax<br>`N` = No Tax<br>`O` = Tax Offset Transaction<br>`R` = Reverse Tax Offset Transaction<br>`P` = DPM Request Tax Offset Transaction<br>`D` = Deferred Tax Offset Transaction |
| 12 | `IsAcq` | Is Acquisition Tax | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 13 | `Isdeferred` | Deferred Tax [Yes/No] | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 14 | `ValueDate` | Due Date for Payment | Date | 8 | - |  |  |
| 15 | `VatPercent` | VAT Percent | Num | 19.6 | - |  |  |
| 16 | `NdPercent` | Non Deductible % | Num | 19.6 | - |  |  |
| 17 | `EqPercent` | Equalization Percent | Num | 19.6 | - |  |  |
| 18 | `BaseObjTyp` | Base Object Type | nVarChar | 20 | - | -1 | `-1`<br>`15` = Delivery notes<br>`16` = Revert Delivery Notes<br>`17` = Sales Order<br>`20` = Goods Receipt<br>`21` = Goods Return<br>`22` = Purchase order<br>`23` = Sales Quotation<br>`112` = Document Draft<br>`59` = Goods Receipt<br>`60` = Goods Issue<br>`28` = Journal Batches<br>`140` = Payment Draft<br>`123` = Checks for Payment Drafts<br>`540000006` = Purchase Quotation |
| 19 | `BaseAbs` | Base Document Internal No. | Int | 11 | - | -1 |  |
| 20 | `BaseArrTyp` | Base Array Type | Int | 11 | - | -1 | `-1` = Default<br>`1` = Main<br>`12` = Array1<br>`13` = Array2<br>`14` = Array3<br>`15` = Array4<br>`16` = Array5<br>`17` = Array6<br>`18` = Array7<br>`24` = Array13 |
| 21 | `BaseLinNum` | Base Row Number | Int | 11 | - | -1 |  |
| 22 | `BaseGrpNum` | Base Group No. | Int | 11 | - | -1 | `-1` = Default<br>`0` = Group1<br>`1` = Group2<br>`2` = Group3 |
| 23 | `BaseSum` | Base Sum | Num | 19.6 | - |  |  |
| 24 | `BaseSumSc` | Base Sum (SC) | Num | 19.6 | - |  |  |
| 25 | `BaseSumFc` | Base Sum (FC) | Num | 19.6 | - |  |  |
| 26 | `VatSum` | VAT Sum | Num | 19.6 | - |  |  |
| 27 | `VatSumSc` | VAT Sum (SC) | Num | 19.6 | - |  |  |
| 28 | `VatSumFc` | VAT Sum (FC) | Num | 19.6 | - |  |  |
| 29 | `DeductSum` | Deduct VAT Sum | Num | 19.6 | - |  |  |
| 30 | `DedctSumSC` | Deduct VAT Sum (SC) | Num | 19.6 | - |  |  |
| 31 | `DedctSumFC` | Deduct VAT Sum (FC) | Num | 19.6 | - |  |  |
| 32 | `EqSum` | Equalization Sum | Num | 19.6 | - |  |  |
| 33 | `EqSumSC` | Equalization Sum (SC) | Num | 19.6 | - |  |  |
| 34 | `EqSumFC` | Equalization Sum (FC) | Num | 19.6 | - |  |  |
| 35 | `TaxAcct` | Tax Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 36 | `DefAcct` | Deferred Tax Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 37 | `NdAcct` | Non Deduct. Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 38 | `AcqAcct` | Acquisition Tax Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 39 | `ExpAcct` | Expense Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 40 | `CrditDebit` | Credit Or Debit Transaction | VarChar | 1 | - |  | `C` = Credit<br>`D` = DEBIT |
| 41 | `PostingTyp` | Sales or Purchasing | VarChar | 1 | - | N | `N` = None<br>`R` = Sales<br>`P` = Purchase |
| 42 | `BasePaid` | Applied Base Sum | Num | 19.6 | - |  |  |
| 43 | `BasePaidSC` | Applied Base Sum SC | Num | 19.6 | - |  |  |
| 44 | `BasePaidFC` | Applied Base Sum FC | Num | 19.6 | - |  |  |
| 45 | `VatPaid` | Applied VAT Sum | Num | 19.6 | - |  |  |
| 46 | `VatPaidSC` | Applied VAT Sum SC | Num | 19.6 | - |  |  |
| 47 | `VatPaidFC` | Applied VAT Sum FC | Num | 19.6 | - |  |  |
| 48 | `DeductPaid` | Applied Deduct Sum | Num | 19.6 | - |  |  |
| 49 | `DdctPaidSC` | Applied Deduct Sum SC | Num | 19.6 | - |  |  |
| 50 | `DdctPaidFC` | Applied Deduct Sum FC | Num | 19.6 | - |  |  |
| 51 | `EqPaid` | Applied Equalization Sum | Num | 19.6 | - |  |  |
| 52 | `EqPaidSC` | Applied Equalization Sum SC | Num | 19.6 | - |  |  |
| 53 | `EqPaidFC` | Applied Equalization Sum FC | Num | 19.6 | - |  |  |
| 54 | `TransAcct` | Transaction Acccount | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 55 | `LnDataNum` | Line Number in Tax Data | Int | 11 | - | -1 |  |
| 56 | `InPrice` | Included in Price | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 57 | `Exempt` | Exempt | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 58 | `InGrossRev` | Included in Gross Revenue | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 59 | `PostStatus` | Posting Status | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 60 | `IsItmLevel` | Is Item Level Tax | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 61 | `MinTAmt` | Min. Taxable Amount | Num | 19.6 | - |  |  |
| 62 | `MinTAmtSC` | Min. Taxable Amount (SC) | Num | 19.6 | - |  |  |
| 63 | `MinTAmtFC` | Min. Taxable Amount (FC) | Num | 19.6 | - |  |  |
| 64 | `MaxTAmt` | Max. Taxable Amount | Num | 19.6 | - |  |  |
| 65 | `MaxTAmtSC` | Max. Taxable Amount (SC) | Num | 19.6 | - |  |  |
| 66 | `MaxTAmtFC` | Max. Taxable Amount (FC) | Num | 19.6 | - |  |  |
| 67 | `FlatTAmt` | Flat Tax Amount | Num | 19.6 | - |  |  |
| 68 | `FlatTAmtSC` | Flat Tax Amount (SC) | Num | 19.6 | - |  |  |
| 69 | `FlatTAmtFC` | Flat Tax Amount (FC) | Num | 19.6 | - |  |  |
| 70 | `EqTaxAcct` | Equalization Tax Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 71 | `Reposted` | Reposted in Transfer Wizard | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 72 | `Unencumbrd` | Unencumbered | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 73 | `IsSplitPay` | Split Payment | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 74 | `SplitPayAc` | Split Payment Account | nVarChar | 15 | - |  |  |
| 75 | `TaxOnRI` | Tax On Reserve Invoice | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 76 | `RvsChrgPrc` | Reverse Charge % | Num | 19.6 | - |  |  |
| 77 | `RvsChrgSum` | Reverse Charge Sum | Num | 19.6 | - |  |  |
| 78 | `RvsChrgSC` | Reverse Charge Sum (SC) | Num | 19.6 | - |  |  |
| 79 | `RvsChrgFC` | Reverse Charge Sum (FC) | Num | 19.6 | - |  |  |
| 80 | `GstPayAct` | GST Payable Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 81 | `RvsPaid` | Applied Reverse Charge Sum | Num | 19.6 | - |  |  |
| 82 | `RvsPaidSC` | Applied Reverse Charge (SC) | Num | 19.6 | - |  |  |
| 83 | `RvsPaidFC` | Applied Reverse Charge (FC) | Num | 19.6 | - |  |  |
| 84 | `InFirstIns` | Included in First Installment | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 85 | `GstRecvAct` | GST Receivable Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 86 | `IsCstmAct` | Apply Customer Accounting Tax Rule | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 87 | `CAOutCode` | Customer Accounting Output Tax Code | nVarChar | 8 | - |  |  |
| 88 | `CABasSum` | Customer Accounting Reverse Base Sum | Num | 19.6 | - |  |  |
| 89 | `CABasSumSc` | Customer Accounting Reverse Base Sum (SC) | Num | 19.6 | - |  |  |
| 90 | `CABasSumFc` | Customer Accounting Reverse Base Sum (FC) | Num | 19.6 | - |  |  |
| 91 | `CAVatSum` | Customer Accounting Reverse VAT Sum | Num | 19.6 | - |  |  |
| 92 | `CAVatSumSc` | Customer Accounting Reverse VAT Sum (SC) | Num | 19.6 | - |  |  |
| 93 | `CAVatSumFc` | Customer Accounting Reverse VAT Sum (FC) | Num | 19.6 | - |  |  |
| 94 | `CAOutAcct` | Customer Accounting Output Tax Account | nVarChar | 15 | - |  |  |
| 95 | `ExtVatPcnt` | External VAT Percent | Num | 19.6 | - |  |  |
| 96 | `ExtVatSum` | External VAT Amount | Num | 19.6 | - |  |  |
| 97 | `VatSumSrc` | VAT Sum Source | VarChar | 1 | - | S | `S` = Internal System Calculation<br>`E` = External Calculation |
| 98 | `ExtVatSumF` | External VAT Amount (FC) | Num | 19.6 | - |  |  |
| 99 | `ExtVatSumS` | External VAT Amount (SC) | Num | 19.6 | - |  |  |
| 100 | `AcqRevTax` | Acquisition/Reverse Corresponding Tax Code | nVarChar | 8 | - |  |  |
| 101 | `VatExmPrc` | VAT Exemption % | Num | 19.6 | - |  |  |
| 102 | `VatExmBase` | VAT Base % | Num | 19.6 | - |  |  |
| 103 | `RevCharge` | Reverse Charge | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineSeq |
