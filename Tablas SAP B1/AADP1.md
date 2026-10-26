# AADP1 - Object Settings - History

- **Tabla:** AADP1
- **Descripción:** Object Settings - History
- **Cantidad de campos:** 80
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AADP1.html

## Campos (80)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `PrintId` | Print No. | nVarChar | 4 | [OADP](OADP.md) |  |  |
| 2 | `ObjType` | Object Type | nVarChar | 11 | - | 13 | `1470000049` = Capitalization<br>`1470000071` = Depreciation Run<br>`1470000090` = Fixed Asset Transfer<br>`23` = Sales Quotation<br>`17` = Sales Order<br>`15` = Delivery<br>`234000031` = Return Request<br>`16` = Returns<br>`203` = A/R Down Payment<br>`13` = A/R Invoice<br>`165` = A/R Correction Invoice<br>`166` = A/R Correction Invoice Reversal<br>`14` = A/R Credit Memo<br>`1470000113` = Purchase Request<br>`540000006` = Purchase Quotation<br>`22` = Purchase Order<br>`20` = Goods Receipt PO<br>`234000032` = Goods Return Request<br>`21` = Goods Return<br>`204` = A/P Down Payment<br>`18` = A/P Invoice<br>`163` = A/P Correction Invoice<br>`164` = A/P Correction Invoice Reversal<br>`19` = A/P Credit Memo<br>`69` = Landed Costs<br>`24` = Incoming Payment<br>`25` = Deposit<br>`46` = Outgoing Payment<br>`76` = Postdated Deposit<br>`57` = Check for Payment<br>`30` = Journal Entry<br>`28` = Journal Voucher<br>`140000010` = Incoming Excise Invoice<br>`140000009` = Outgoing Excise Invoice<br>`59` = Goods Receipt<br>`60` = Goods Issue<br>`1250000001` = Inventory Transfer Request<br>`67` = Inventory Transfer<br>`68` = Work Instructions<br>`202` = Production Order<br>`162` = Inventory Revaluation<br>`156` = Pick List<br>`1470000065` = Inventory Counting<br>`10000071` = Inventory Posting<br>`310000001` = Inventory Opening Balances<br>`191` = Service Call<br>`190` = Service Contract<br>`176` = Equipment Card<br>`88` = Entrada<br>`89` = Salida<br>`90` = Traspaso<br>`132` = Correction Invoice<br>`234000021` = Project Management Document |
| 3 | `Copies` | No. of Copies | Int | 6 | - | 1 |  |
| 4 | `PrintOnAdd` | Add & Print | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `ExprtOnAdd` | Add & Export | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `RoundSums` | Rounding Amounts | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `Remark` | Standard Remarks | Text | 16 | - |  |  |
| 8 | `PrintSums` | Print Totals | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 9 | `VndrNum` | Print Mfr Catalog No. | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 10 | `PrnDscnt` | Print Discount Data | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 11 | `SplitTran1` | Split Transaction 1 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 12 | `SplitTran2` | Split Transaction 2 | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 13 | `SplitTran3` | Split Transaction 3 | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 14 | `ShowBothNu` | Print Mfr Catalog No. Instead | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 15 | `BaseRmrk` | Display Base Remarks | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 16 | `HandCopies` | No. of Copies for Manual Doc. | Int | 6 | - | 1 |  |
| 17 | `EngKBItem` | Switch to English Keyboard when Entering an Item | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 18 | `EngKBCard` | Switch to English Keyboard When Entering a BP | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 19 | `OrdrPicDef` | Set Pick Order as Default | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 20 | `SpltTrBOE1` | Split Bill of Exchange Transaction | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 21 | `LineNumPPg` | Row Item Number Per Page | Int | 6 | - | 5 |  |
| 22 | `JENumPPg` | Journal Entry Number Per Page | Int | 6 | - | 2 |  |
| 23 | `CashPay` | Remark for Cash Payments | Text | 16 | - |  |  |
| 24 | `NonCashPay` | Remark for Non-Cash Payments | Text | 16 | - |  |  |
| 25 | `MaxUOPay` | Max. Under/Overpayment Amount | Num | 19.6 | - |  |  |
| 26 | `CkeckPaper` | Paper for Checks | VarChar | 1 | - | S | `B` = Blank Paper<br>`S` = Overflow Check Stock<br>`P` = Overflow Blank Paper |
| 27 | `AllowFuPos` | Allow Future Posting | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 28 | `ErdOutMode` | ERD Mode for Outgoing Payments | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 29 | `ErdIncMode` | ERD Mode for Incoming Payments | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 30 | `ChkDupRef` | Check Duplicate BP Reference Number | VarChar | 1 | - | N | `N` = Without Warning<br>`W` = Warning Only<br>`B` = Block Release |
| 31 | `CpyCVRef` | Copy BP Reference Number | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 32 | `BatchSerPr` | Batch/Serial No. Print Definitions | VarChar | 1 | - | A | `A` = Document and Batch/Serial No.<br>`D` = Document Only<br>`B` = Batch/Serial No. Only |
| 33 | `YearTrans` | Display Transaction in Payment | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 34 | `ReconJeSer` | Reconciliation JE Series | Int | 6 | - | 0 |  |
| 35 | `ReopOrder` | Enable Reopen Orders by Return | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 36 | `ForceReOrd` | Always Reopen Orders by Return | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 37 | `PrintRows` | Print Rows | VarChar | 1 | - | A | `A` = All Rows<br>`M` = All Modified Rows<br>`T` = Modified Rows Excl. Tax Amount |
| 38 | `orderblock` | Block Early Posting Date | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 39 | `RecomPkg` | Recommend Packaging | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 40 | `Enitemcost` | Enable Setting Item Cost | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 41 | `ClosePQ` | Close Related PQ | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 42 | `CpyPRPrice` | Enable Copying PR Price | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 43 | `EnSetCost` | Enable Setting Cost By Default | VarChar | 1 | - | N |  |
| 44 | `DftPLChk` | Default Price List Check | VarChar | 1 | - | N |  |
| 45 | `DfltPLSel` | Default Price List Selection | Int | 6 | - | -1 |  |
| 46 | `EmailOnAdd` | Add & Email | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 47 | `PDFOnAdd` | Add & Export to PDF | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 48 | `EmailSbj` | E-Mail Subject | nVarChar | 254 | - |  |  |
| 49 | `EmailBody` | Email Body | Text | 16 | - |  |  |
| 50 | `BlockWHT08` | Block Payment in Local Currency WHT 08 | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 51 | `BlockExprt` | Block Export to Word | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 52 | `BlockPrint` | Block Printing Documents | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 53 | `BlockMail` | Block Email Document | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 54 | `BlockToPDF` | Block Export to PDF | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 55 | `BlockFax` | Block Sent to Fax | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 56 | `PoDropPrss` | PO Drop-Ship Process | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 57 | `ShowCash` | Allow Cash Accounts Only | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 58 | `PRUseBPTax` | Purchase Request use BP Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 59 | `EnblTtlEgD` | Apply Exchange Rate of Drawn Down Payments | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 60 | `EnblUpdUDF` | Enable Updating UDF | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 61 | `EnblDpmTax` | Enable Tax Calculation in Down Payment Invoices | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 62 | `ChkRefBP` | Validate on Customer Level | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 63 | `ChkRefYear` | Validate on Fiscal Year Level | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 64 | `BspDpmType` | Down Payment Type for BSP | VarChar | 1 | - | E | `E`<br>`R` = Down Payment Request<br>`I` = Down Payment Invoice |
| 65 | `ReopenByC` | Enable the Displaying of Base Document Items When Target Documents Are Canceled | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 66 | `ForceReByC` | Always Display Base Document Items When Target Documents Are Canceled | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 67 | `OpenSnB` | Open SnB form for Bin First Item when Auto Allocation | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 68 | `BItmDscUpd` | Block Item Description Updated in the Copied Lines | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 69 | `DeferrTax` | Deferred Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 70 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 71 | `CtlActSlct` | Allow Control Account Selection | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 72 | `SepDiscDpm` | Separate Discount % and DPM % Fields | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 73 | `DiffCigCup` | Allow Different CIG and CUP Codes in One Payment | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 74 | `NotDeferTa` | Do Not Apply Deferred Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 75 | `EmailSignD` | E-Mail Signed Document | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 76 | `DftPriList` | Default Price List | Int | 6 | - |  |  |
| 77 | `PackSlip` | Print Packing Slip | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 78 | `TermsPrn` | Print Terms and Conditions | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 79 | `WarrPrn` | Print Warranties Policy | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 80 | `ReturnPrn` | Print Returns Policy | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | PrintId, ObjType, LogInstanc |
