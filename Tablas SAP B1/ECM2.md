# ECM2 - Electronic Transactions

- **Tabla:** ECM2
- **Descripción:** Electronic Transactions
- **Cantidad de campos:** 43
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ECM2.html

## Campos (43)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal ID | Int | 11 | - |  |  |
| 2 | `Code` | Code | Int | 11 | [OECM](OECM.md) |  | `0` = Invalid<br>`1` = GEN<br>`2` = EET<br>`3` = CFDI<br>`4` = FPA<br>`5` = MTD<br>`6` = EWB<br>`7` = PEPPOL<br>`8` = HOI<br>`9` = MYF<br>`10` = EIS<br>`11` = IIS<br>`12` = IIS_ANNUAL<br>`13` = DIGIPOORT<br>`14` = E-Books<br>`15` = DOX<br>`16` = RTIE<br>`17` = E-Billing<br>`18` = Tax Service<br>`19` = AFE<br>`20` = Document Signature<br>`21` = KSeF<br>`22` = GSTReturn<br>`23` = PT Document Signature<br>`24` = Skat DK<br>`25` = EII<br>`26` = NFe<br>`27` = PT eInvoicing<br>`28` = PT Electronic Communications<br>`29` = Veri*factu<br>`30` = BAS<br>`31` = PDF with XML Attachment<br>`32` = FReINV<br>`33` = euBP<br>`34` = ILOI<br>`35` = EDGT<br>`36` = EDCR<br>`37` = NAV |
| 3 | `ParentID` | Parent ID | Int | 11 | [ECM2](ECM2.md) |  |  |
| 4 | `ActType` | Action Type | Int | 11 | - | 0 | `1` = Setup<br>`2` = Report<br>`3` = A/R Document<br>`4` = A/P Document<br>`5` = A/R Draft Document<br>`6` = A/P Draft Document<br>`7` = Other<br>`8` = Skip<br>`9` = Contingency<br>`10` = BP Check<br>`11` = Incoming Payment<br>`12` = Outgoing Payment<br>`13` = Internal Reconciliation<br>`14` = Transportation Document<br>`15` = Inventory Transfer<br>`16` = VAT Obligations<br>`17` = VAT Declarations<br>`18` = VAT Liabilities<br>`19` = VAT Payments<br>`20` = Delivery<br>`21` = Return<br>`22` = A/R Invoice<br>`23` = A/R Credit Memo<br>`24` = Goods Receipt PO<br>`25` = Goods Return<br>`26` = A/P Invoice<br>`27` = A/P Credit Memo<br>`28` = Draft Incoming Payment<br>`29` = Draft Outgoing Payment<br>`30` = Journal Entry<br>`31` = E-Books Expense<br>`35` = Company VAT Calendar<br>`36` = Provisional VAT Returns<br>`37` = Receipts for VAT Returns<br>`38` = A/R Invoice<br>`39` = A/R Credit Memo<br>`40` = Delivery<br>`41` = A/R Invoice Based on Delivery<br>`42` = Series<br>`43` = Invoices<br>`44` = Goods Transfers<br>`45` = Goods Issue<br>`46` = Goods Receipt<br>`47` = Pick List<br>`48` = Draft Goods Issue<br>`49` = Draft Goods Receipt<br>`50` = Request CAEA |
| 5 | `ActDesc` | Action Description | nVarChar | 100 | - |  |  |
| 6 | `ActStatus` | Action Status | VarChar | 1 | - | N | `N` = New<br>`P` = Pending<br>`E` = Error<br>`T` = Temporary Error<br>`O` = OK<br>`S` = Sent<br>`R` = Document Error<br>`W` = Waiting<br>`A` = Authorized<br>`I` = In Process<br>`J` = Rejected<br>`D` = Denied<br>`C` = Canceled<br>`B` = Aborted<br>`Q` = Queued<br>`M` = Imported<br>`G` = Warning<br>`V` = Approved<br>`F` = Approving<br>`H` = Rejecting<br>`K` = Generated<br>`Y` = Ready to Process<br>`L` = Determined<br>`X` = Importing<br>`Z` = Response Updated<br>`i` = In Process to Intermediary<br>`s` = Sent to Intermediary<br>`v` = Approved by Intermediary<br>`g` = Not Integrated with Customer<br>`c` = Not Sent to Customer<br>`x` = Error Sending to Customer<br>`t` = Sent to Customer<br>`r` = Received by Customer<br>`j` = Rejected by Customer<br>`p` = Paid by Customer<br>`l` = Checking Integration Status<br>`o` = Not Approved<br>`e` = Reverse Charge<br>`u` = Continued<br>`f` = Further Objection<br>`a` = Cancelling<br>`n` = Continuing<br>`b` = Further Objection in Progress<br>`d` = Resending<br>`w` = Pending to CAEA<br>`k` = Queued<br>`z` = Updating Response<br>`m` = Disputing<br>`y` = Dispute |
| 7 | `IsRemoved` | Is Removed | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `ActMessage` | Action Message | nVarChar | 254 | - |  |  |
| 9 | `ActEnv` | Action Environment Type | Int | 11 | [OBNI](OBNI.md) | -1 |  |
| 10 | `BPLId` | Branch ID | Int | 11 | [OBPL](OBPL.md) | -1 |  |
| 11 | `Submits` | Report - Number of Submissions | Int | 6 | - |  |  |
| 12 | `ObjectID` | Object ID | nVarChar | 50 | - |  |  |
| 13 | `ReportID` | Report ID | nVarChar | 50 | - |  |  |
| 14 | `SrcObjType` | Source Object Type | nVarChar | 20 | - |  |  |
| 15 | `SrcObjAbs` | Source Object Internal ID | Int | 11 | - |  |  |
| 16 | `Cancel` | Cancelation | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 17 | `AssignedID` | Assigned ID | nVarChar | 100 | - |  |  |
| 18 | `DocBtch` | Document Batch | nVarChar | 50 | - |  |  |
| 19 | `DocBtchLn` | Document Batch Line | Int | 6 | - |  |  |
| 20 | `GenType` | Generation Type | VarChar | 1 | - | N | `N` = Not Relevant<br>`G` = Generate<br>`L` = Generate - Later<br>`F` = Generate - Offline<br>`S` = Send<br>`R` = Send - Later |
| 21 | `TestMode` | Test Mode | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 22 | `PeriodType` | Report Period Type | VarChar | 1 | - |  | Ignore<br>`Y` = Year<br>`Q` = Quarter<br>`M` = Month<br>`P` = Period |
| 23 | `PeriodNum` | Report Period Number | Int | 11 | - |  |  |
| 24 | `Year` | Report Year | Int | 6 | - |  |  |
| 25 | `DateFrom` | Report - Date From | Date | 8 | - |  |  |
| 26 | `DateTo` | Report - Date To | Date | 8 | - |  |  |
| 27 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 28 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 29 | `CreateTS` | Creation Time - Incl. Secs | Int | 11 | - |  |  |
| 30 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 31 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 32 | `UpdateTS` | Update Time - Incl. Secs | Int | 11 | - |  |  |
| 33 | `LogInstanc` | Log Instance | Int | 6 | - |  |  |
| 34 | `SchedJobID` | Scheduled Job ID | Int | 11 | [OBSJ](OBSJ.md) |  |  |
| 35 | `GUID` | GUID | nVarChar | 100 | - |  |  |
| 36 | `Authority` | Authority Code | nVarChar | 16 | [OPAC](OPAC.md) |  |  |
| 37 | `CancStatus` | Cancelation Status | VarChar | 1 | - | T | `T`<br>`N` = New Request<br>`S` = Request Sent<br>`A` = Approved<br>`R` = Rejected<br>`E` = Error<br>`C` = Canceled<br>`I` = In Process<br>`U` = Sent To Authorities<br>`W` = Canceled Without Approval |
| 38 | `EDocType` | E-Doc Type | Int | 11 | [OUNCL](OUNCL.md) |  |  |
| 39 | `EDocNum` | E-Doc Number | nVarChar | 100 | - |  |  |
| 40 | `ProcTarget` | Processing Target/Source | nVarChar | 40 | - |  |  |
| 41 | `Emergency` | Emergency | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 42 | `SttsReason` | Status Reason | nVarChar | 3 | - |  | `NON` = No Issues<br>`REF` = Incorrect references<br>`LEG` = Incorrect legal information<br>`REC` = Unknown receiver<br>`QUA` = Insufficient item quality<br>`DEL` = Issues with delivery<br>`PRI` = Incorrect prices<br>`QTY` = Incorrect quantity<br>`ITM` = Incorrect items<br>`PAY` = Incorrect payment terms<br>`UNR` = Not recognized<br>`FIN` = Incorrect financials<br>`PPD` = Partially Paid<br>`OTH` = Other |
| 43 | `SttsDescr` | Status Description | nVarChar | 254 | - |  |  |

## Claves e índices (4)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| ACTION | Yes | Code, AbsEntry |
| DOCREF | No | SrcObjType, SrcObjAbs, Code |
| GUID | Yes | GUID |
