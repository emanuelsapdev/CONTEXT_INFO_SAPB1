# OPWZ - Payment Wizard

- **Tabla:** OPWZ
- **Descripción:** Payment Wizard
- **Cantidad de campos:** 77
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OPWZ.html

## Campos (77)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `IdNumber` | ID Number | Int | 11 | - |  |  |
| 2 | `PmntDate` | Date of Payment Run | Date | 8 | - |  |  |
| 3 | `NextDate` | A/P Due Date To | Date | 8 | - |  |  |
| 4 | `OutgoType` | Outgoing Type | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `IncomType` | Incoming Type | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `CheckPmntM` | Check Payment Terms | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `BnkTrnsPmM` | Bank Transfer Payment Terms | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `FilePath` | File Path | Text | 16 | - |  |  |
| 9 | `PostDtFrom` | Posting Date From | Date | 8 | - |  |  |
| 10 | `PostDtTo` | Posting Date To | Date | 8 | - |  |  |
| 11 | `ValDteFrom` | Due Date From | Date | 8 | - |  |  |
| 12 | `ValDateTo` | Due Date To | Date | 8 | - |  |  |
| 13 | `ApInvAmntF` | A/P Invoice Amount From | Num | 19.6 | - |  |  |
| 14 | `ApInvAmntT` | A/P Invoice Amount To | Num | 19.6 | - |  |  |
| 15 | `PchNoFrom` | A/P Invoice No. From | Int | 11 | - |  |  |
| 16 | `PchNoTo` | A/P Invoice No. To | Int | 11 | - |  |  |
| 17 | `InvNoFrom` | A/R Invoice No. From | Int | 11 | - |  |  |
| 18 | `InvNoTo` | A/R Invoice No. To | Int | 11 | - |  |  |
| 19 | `SelPriorit` | Selection Priority | Int | 11 | - |  |  |
| 20 | `Status` | Object Status | VarChar | 1 | - | S | `S` = Saved Wizard<br>`R` = Recommended Wizard<br>`E` = Executed Wizard<br>`H` = Scheduled Wizard<br>`L` = Scheduled Executing Wizard<br>`D` = Payment Order Run |
| 21 | `WizardName` | Wizard Name | nVarChar | 100 | - |  |  |
| 22 | `StatusDisc` | Status | nVarChar | 100 | - |  |  |
| 23 | `Canceled` | Canceled | VarChar | 1 | - | N |  |
| 24 | `BoePmnMn` | Bill of Exchange Paymt Method | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 25 | `SeriesOut` | Outgoing Series | Int | 11 | [NNM1](NNM1.md) | 0 |  |
| 26 | `SeriesIn` | Incoming Series | Int | 11 | [NNM1](NNM1.md) | 0 |  |
| 27 | `TotalOut` | Total Outgoing | Num | 19.6 | - |  |  |
| 28 | `TotalIn` | Total Incoming | Num | 19.6 | - |  |  |
| 29 | `ViewIntBal` | Include Interim Acct Balance | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 30 | `SelMthd` | Selection Method | VarChar | 1 | - | D | `M` = By Monthly Invoice<br>`D` = By Document Property |
| 31 | `MINumFrom` | Monthly Invoice No. From | Int | 11 | - |  |  |
| 32 | `MINumTo` | Monthly Invoice No. To | Int | 11 | - |  |  |
| 33 | `MIDateFrom` | Monthly Invoice Issued Date From | Date | 8 | - |  |  |
| 34 | `MIDateTo` | Monthly Invoice Issued Date To | Date | 8 | - |  |  |
| 35 | `MIVNumFrom` | A/P Monthly Invoice No. From | Int | 11 | - |  |  |
| 36 | `MIVNumTo` | A/P Monthly Invoice No. To | Int | 11 | - |  |  |
| 37 | `MIVDateFro` | A/P Monthly Invoice Date From | Date | 8 | - |  |  |
| 38 | `MIVDateTo` | A/P Monthly Invoice Date To | Date | 8 | - |  |  |
| 39 | `APDocDtFrm` | A/P Document Date From | Date | 8 | - |  |  |
| 40 | `APDocDtTo` | A/P Document Date To | Date | 8 | - |  |  |
| 41 | `APDueDtFrm` | A/P Due Date From | Date | 8 | - |  |  |
| 42 | `NxtPmntDat` | Next Payment Run Date | Date | 8 | - |  |  |
| 43 | `MinPayAR` | Minimum Incoming Payment | Num | 19.6 | - |  |  |
| 44 | `MinPayAP` | Minimum Outgoing Payment | Num | 19.6 | - |  |  |
| 45 | `ShowAtCard` | Display BP Ref. No. | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 46 | `TolerDays` | Tolerance Days | Int | 6 | - |  |  |
| 47 | `MinCashDis` | Min. Cash Discount | Num | 19.6 | - |  |  |
| 48 | `NegBalBP` | Include Negative Balance BP | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 49 | `ManualJE` | Include Manual JEs | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 50 | `NegTrans` | Include Negative Transactions | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 51 | `CDTransApp` | Apply to Cash Discount Trans. | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 52 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 53 | `CigTo` | Contract Code ID To | Int | 11 | [OCIG](OCIG.md) |  |  |
| 54 | `CupFrom` | Unique Code of Project From | Int | 11 | [OCUP](OCUP.md) |  |  |
| 55 | `CupTo` | Unique Code of Project To | Int | 11 | [OCUP](OCUP.md) |  |  |
| 56 | `CigFrom` | Contract Code ID From | Int | 11 | [OCIG](OCIG.md) |  |  |
| 57 | `BPLId` | Active Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 58 | `BoeDDFrom` | BoE Due Date From | Date | 8 | - |  |  |
| 59 | `BoeDDTo` | BoE Due Date To | Date | 8 | - |  |  |
| 60 | `BoeNumFrom` | BoE No. From | Int | 11 | [OBOE](OBOE.md) |  |  |
| 61 | `BoeNumTo` | BoE No. To | Int | 11 | [OBOE](OBOE.md) |  |  |
| 62 | `BoeStatus` | Bill of Exchange Status | nVarChar | 32 | - |  |  |
| 63 | `HaExistBoe` | Handle Existing BoE | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 64 | `SeriesPOO` | Outgoing Payment Order Series | Int | 11 | [NNM1](NNM1.md) | 0 |  |
| 65 | `SeriesPOI` | Incoming Payment Order Series | Int | 11 | [NNM1](NNM1.md) | 0 |  |
| 66 | `SeqType` | Sequence Type | nVarChar | 4 | - |  | `OOFF` = OOFF<br>`FRST` = FRST<br>`RCUR` = RCUR<br>`FNAL` = FNAL |
| 67 | `PayDueDate` | Payment Due Date Determination | VarChar | 1 | - | R | `R` = Run Date<br>`D` = Document Due Date |
| 68 | `CentrPay` | Centralized Payment | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 69 | `BA_AP_From` | A/P Blanket Agreement From | Int | 11 | - |  |  |
| 70 | `BA_AP_To` | A/P Blanket Agreement To | Int | 11 | - |  |  |
| 71 | `BA_AR_From` | A/R Blanket Agreement From | Int | 11 | - |  |  |
| 72 | `BA_AR_To` | A/R Blanket Agreement To | Int | 11 | - |  |  |
| 73 | `JobId` | Job ID Number | Int | 11 | - |  |  |
| 74 | `ZeroBalBP` | Include Zero Balance BP | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 75 | `ZeroBalDoc` | Zero Balance Document Types | nVarChar | 50 | - | YNNNNYNNNNN |  |
| 76 | `VersionNum` | Version Number | nVarChar | 13 | - |  |  |
| 77 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Update<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | IdNumber |
| NAME | Yes | WizardName |
