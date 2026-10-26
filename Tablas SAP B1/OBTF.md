# OBTF - Journal Voucher Entry

- **Tabla:** OBTF
- **Descripción:** Journal Voucher Entry
- **Cantidad de campos:** 116
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBTF.html

## Campos (116)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `BatchNum` | Journal Voucher No. | Int | 11 | [OBTD](OBTD.md) |  |  |
| 2 | `TransId` | Transaction Number | Int | 11 | - |  |  |
| 3 | `BtfStatus` | Status | VarChar | 1 | - | O | `O` = Open<br>`C` = Closed |
| 4 | `TransType` | Origin | nVarChar | 20 | - | -1 | `16` = Returns<br>`203` = A/R Down Payment<br>`15` = Delivery<br>`13` = A/R Invoice<br>`165` = A/R Correction Invoice<br>`166` = A/R Correction Invoice Reversal<br>`14` = A/R Credit Memo<br>`132` = Correction Invoice<br>`20` = Goods Receipt PO<br>`21` = Goods Return<br>`204` = A/P Down Payment<br>`18` = A/P Invoice<br>`163` = A/P Correction Invoice<br>`164` = A/P Correction Invoice Reversal<br>`19` = A/P Credit Memo<br>`281` = A/P Tax Invoice<br>`69` = Landed Costs<br>`140000009` = Outgoing Excise Invoice<br>`140000010` = Incoming Excise Invoice<br>`254000065` = Self Invoice<br>`254000066` = Self Credit Memo<br>`10000079` = TDS Adjustment<br>`24` = Incoming Payment<br>`25` = Deposit<br>`46` = Vendor Payment<br>`57` = Checks for Payment<br>`76` = Postdated Deposit<br>`182` = BoE Transaction<br>`-2` = Opening Balance<br>`-3` = Closing Balance<br>`321` = Internal Reconciliation<br>`10000046` = Data Archive<br>`30` = Journal Entry<br>`58` = Inventory List<br>`59` = Goods Receipt<br>`60` = Goods Issue<br>`67` = Inventory Transfers<br>`68` = Work Instructions<br>`162` = Inventory Valuation<br>`202` = Production Order<br>`1470000049` = Fixed Asset Capitalization<br>`1470000060` = Fixed Asset Capitalization Credit Memo<br>`1470000094` = Fixed Asset Retirement<br>`1470000075` = Fixed Asset Manual Depreciation<br>`1470000090` = Fixed Asset Transfer<br>`1470000085` = Fixed Asset Revaluation<br>`-1` = All Transactions<br>`310000001` = Inventory Opening Balance<br>`10000071` = Inventory Posting<br>`254000061` = Input Service Distribution Invoice<br>`254000062` = Input Service Distribution Recipient Invoice<br>`254000063` = Input Service Distribution Credit Memo<br>`254000064` = Input Service Distribution Recipient Credit Memo<br>`-4` = Adj. for Manual Ext. Reconciliation |
| 5 | `BaseRef` | Origin No. | nVarChar | 11 | - |  |  |
| 6 | `RefDate` | Posting Date | Date | 8 | - |  |  |
| 7 | `Memo` | Remarks | nVarChar | 254 | - |  |  |
| 8 | `Ref1` | Reference 1 | nVarChar | 200 | - |  |  |
| 9 | `Ref2` | Reference 2 | nVarChar | 200 | - |  |  |
| 10 | `CreatedBy` | Origin | Int | 11 | - |  |  |
| 11 | `LocTotal` | Total in Local Currency | Num | 19.6 | - |  |  |
| 12 | `FcTotal` | Total in Foreign Currency | Num | 19.6 | - |  |  |
| 13 | `SysTotal` | Total in System Currency | Num | 19.6 | - |  |  |
| 14 | `TransCode` | Transaction Code | nVarChar | 4 | [OTRC](OTRC.md) |  |  |
| 15 | `OrignCurr` | Original Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 16 | `TransRate` | Transaction Rate | Num | 19.6 | - |  |  |
| 17 | `BtfLine` | Row in Voucher | Int | 11 | - |  |  |
| 18 | `TransCurr` | Transaction Currency | nVarChar | 3 | - |  |  |
| 19 | `Project` | Project Code | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 20 | `DueDate` | Value Date | Date | 8 | - |  |  |
| 21 | `TaxDate` | Tax Date | Date | 8 | - |  |  |
| 22 | `PCAddition` | PC Addition | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 23 | `FinncPriod` | Posting Period | Int | 11 | [OFPR](OFPR.md) |  |  |
| 24 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 25 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 26 | `CreateDate` | Recording Date | Date | 8 | - |  |  |
| 27 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 28 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 29 | `RefndRprt` | Repayment Report | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 30 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 31 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 30 |  |
| 32 | `Indicator` | Indicator Code | nVarChar | 2 | [OIDC](OIDC.md) |  |  |
| 33 | `AdjTran` | Adjusting Transaction | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 34 | `RevSource` | Revaluation Source | VarChar | 1 | - | N | `F` = FC<br>`S` = System<br>`N` = No |
| 35 | `StornoDate` | Reversal Date | Date | 8 | - |  |  |
| 36 | `StornoToTr` | Reverse Transaction | Int | 11 | - |  |  |
| 37 | `AutoStorno` | Use Auto-Reverse | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 38 | `Corisptivi` | Transaction Values | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 39 | `VatDate` | VAT Date | Date | 8 | - |  |  |
| 40 | `StampTax` | Stamp Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 41 | `Series` | Series | Int | 11 | - | 0 |  |
| 42 | `Number` | Number | Int | 11 | - |  |  |
| 43 | `AutoVAT` | Automatic Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 44 | `DocSeries` | Document Series | Int | 11 | - |  |  |
| 45 | `FolioPref` | Folio Prefix String | nVarChar | 4 | - |  |  |
| 46 | `FolioNum` | Folio Number | Int | 11 | - |  |  |
| 47 | `CreateTime` | Generation Time | Int | 6 | - |  |  |
| 48 | `BlockDunn` | Block Dunning Letter | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 49 | `ReportEU` | Include in EU Report | VarChar | 1 | - | N | `Y` = VAT<br>`N` = No |
| 50 | `Report347` | Include in 347 Report | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 51 | `Printed` | Printed | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 52 | `DocType` | Transact. Type | nVarChar | 60 | [OJET](OJET.md) |  |  |
| 53 | `AttNum` | Number of Attachments | Int | 11 | - | 0 |  |
| 54 | `GenRegNo` | Generate Reg. No. or Not | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 55 | `RG23APart2` | RG23A Part2 No | Int | 11 | - |  |  |
| 56 | `RG23CPart2` | RG23C Part2 No | Int | 11 | - |  |  |
| 57 | `MatType` | Material Type | Int | 11 | - |  |  |
| 58 | `Creator` | Creator Name | nVarChar | 155 | - |  |  |
| 59 | `Approver` | Approver Name | nVarChar | 155 | - |  |  |
| 60 | `Location` | Loc. | Int | 11 | [OLCT](OLCT.md) |  |  |
| 61 | `SeqCode` | Sequence Code | Int | 6 | - |  |  |
| 62 | `Serial` | Serial Number | Int | 11 | - |  |  |
| 63 | `SeriesStr` | Series String | nVarChar | 3 | - |  |  |
| 64 | `SubStr` | Subseries String | nVarChar | 3 | - |  |  |
| 65 | `AutoWT` | Automatic WTax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 66 | `WTSum` | WTax Amount | Num | 19.6 | - |  |  |
| 67 | `WTSumSC` | WTax Amount (SC) | Num | 19.6 | - |  |  |
| 68 | `WTSumFC` | WTax Amount (FC) | Num | 19.6 | - |  |  |
| 69 | `WTApplied` | Applied WTax | Num | 19.6 | - |  |  |
| 70 | `WTAppliedS` | Applied WTax (SC) | Num | 19.6 | - |  |  |
| 71 | `WTAppliedF` | Applied WTax (FC) | Num | 19.6 | - |  |  |
| 72 | `BaseAmnt` | Base Amount | Num | 19.6 | - |  |  |
| 73 | `BaseAmntSC` | Base Amount (SC) | Num | 19.6 | - |  |  |
| 74 | `BaseAmntFC` | Base Amount (FC) | Num | 19.6 | - |  |  |
| 75 | `BaseVtAt` | WTax Base VAT Amount | Num | 19.6 | - |  |  |
| 76 | `BaseVtAtSC` | WTax Base VAT Amount (SC) | Num | 19.6 | - |  |  |
| 77 | `BaseVtAtFC` | WTax Base VAT Amount (FC) | Num | 19.6 | - |  |  |
| 78 | `VersionNum` | Version Number | nVarChar | 13 | - |  |  |
| 79 | `BaseTrans` | Base Transaction Number | Int | 11 | - |  |  |
| 80 | `ResidenNum` | Residence Number | VarChar | 1 | - | 1 | `1` = Spanish Fiscal ID<br>`2` = VAT Registration Number<br>`3` = Passport<br>`4` = Fiscal ID Issued by the Country/Region of Residence<br>`5` = Certificate of Fiscal Residence<br>`6` = Other Document |
| 81 | `OperatCode` | Operation Code | VarChar | 1 | - |  | `A` = Summary Invoices Entry<br>`B` = Summary Receipts Entry<br>`C` = Invoice with Several VAT Rates<br>`D` = Correction Invoice<br>`E` = Due VAT Pending Invoice Issuance<br>`F` = Expenses Incurred by Travel Agent for Customers<br>`G` = Special Regulation for VAT Group<br>`H` = Special Regulation for Gold Investment<br>`I` = Reverse Charge Procedure<br>`J` = Unsummarized Receipts<br>`K` = Identification of Error Transactions<br>`X` = Transactions with Entrepreneurs Issuing Receipts for Agricultural Compensation<br>`N` = Service Invoicing by Travel Agencies on Behalf of Third Parties<br>`R` = Business Office Rental<br>`S` = Subsidies<br>`T` = Incoming Payments for Industrial and Intellectual Property Rights<br>`U` = Insurance Transactions<br>`V` = Purchases from Travel Agencies<br>`W` = Transactions Subject to Production, Service, and Import Taxes in Ceuta and Melilla |
| 82 | `Ref3` | Reference 3 | nVarChar | 200 | - |  |  |
| 83 | `SSIExmpt` | SSI Exemption | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 84 | `SignMsg` | Signature Input Message | Text | 16 | - |  |  |
| 85 | `SignDigest` | Signature Digest | Text | 16 | - |  |  |
| 86 | `CertifNum` | Certification Number | nVarChar | 50 | - |  |  |
| 87 | `KeyVersion` | Private Key Version | Int | 11 | - |  |  |
| 88 | `CUP` | Unique Code of Project | Int | 11 | [OCUP](OCUP.md) |  |  |
| 89 | `CIG` | Contract Code Identification | Int | 11 | [OCIG](OCIG.md) |  |  |
| 90 | `SupplCode` | Supplementary Code | nVarChar | 254 | - |  |  |
| 91 | `SPSrcType` | Service Posting Source Type | Int | 11 | - |  |  |
| 92 | `SPSrcID` | Service Posting Source ID | Int | 11 | - |  |  |
| 93 | `SPSrcDLN` | Service Post. Source Delivery | Int | 11 | - |  |  |
| 94 | `DeferedTax` | Deferred Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 95 | `AgrNo` | Blanket Agreement Number | Int | 11 | [OOAT](OOAT.md) |  |  |
| 96 | `SeqNum` | Sequence Number | Int | 11 | - |  |  |
| 97 | `ECDPosTyp` | ECD Posting Type | VarChar | 1 | - | N | `N` = Normal<br>`E` = Statement |
| 98 | `RptPeriod` | Reporting Period | nVarChar | 5 | - |  |  |
| 99 | `RptMonth` | Reporting Month | Date | 8 | - |  |  |
| 100 | `ExTransId` | Exposed Transaction ID | Int | 11 | - |  |  |
| 101 | `PrlLinked` | Is JE linked by MX Payroll | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 102 | `PTICode` | POI Code | nVarChar | 5 | - |  |  |
| 103 | `Letter` | Letter | VarChar | 1 | - |  |  |
| 104 | `FolNumFrom` | Folio Number From | Int | 11 | - |  |  |
| 105 | `FolNumTo` | Folio Number To | Int | 11 | - |  |  |
| 106 | `RepSection` | Reporting Section | nVarChar | 3 | - |  |  |
| 107 | `ExclTaxRep` | Exclude from Control Statement | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 108 | `IsCoEntry` | Cost Center Transfer form | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 109 | `SAPPassprt` | Extended SAP Passport | Text | 16 | - |  |  |
| 110 | `AtcEntry` | Attachment Entry | Int | 11 | [OATC](OATC.md) |  |  |
| 111 | `Attachment` | Attachment | Text | 16 | - |  |  |
| 112 | `EBookable` | E-Books Enabled | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 113 | `DataVers` | Data Version | Int | 11 | - | 1 |  |
| 114 | `SAFTType` | SAF-T Transaction Type | VarChar | 1 | - | - | `N` = Normal<br>`-` = -<br>`R` = Adjustments of Tax Period<br>`A` = Measurement of Results<br>`J` = Adjustment<br>`I` = Do Not Export |
| 115 | `AllocNum` | Allocation Number for IL | nVarChar | 50 | - |  |  |
| 116 | `SAFTTypeEx` | SAF-T Transaction Type | nVarChar | 10 | [OSTE](OSTE.md) | - |  |

## Claves e índices (4)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | BatchNum, TransId |
| TRANS_TYPE | No | TransType, CreatedBy |
| JDT_NUM | No | TransId |
| BTF_STATUS | No | BtfStatus |
