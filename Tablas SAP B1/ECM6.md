# ECM6 - Electronic Protocol DI API Properties

- **Tabla:** ECM6
- **Descripción:** Electronic Protocol DI API Properties
- **Cantidad de campos:** 118
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ECM6.html

## Campos (118)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Communication Type or Protocol | Int | 11 | [OECM](OECM.md) |  | `0` = Invalid<br>`1` = GEN<br>`2` = EET<br>`3` = CFDI<br>`4` = FPA<br>`5` = MTD<br>`6` = EWB<br>`7` = PEPPOL<br>`8` = HOI<br>`9` = MYF<br>`10` = EIS<br>`11` = IIS<br>`12` = IIS_ANNUAL<br>`13` = DIGIPOORT<br>`14` = E-Books<br>`15` = DOX<br>`16` = RTIE<br>`17` = E-Billing<br>`18` = Tax Service<br>`19` = AFE<br>`20` = Doc. Sign.<br>`21` = KSeF<br>`22` = GSTReturn<br>`23` = PT Doc. Sign.<br>`24` = Skat DK<br>`25` = EII<br>`26` = NFe<br>`27` = PT eInvoicing<br>`28` = PT Electronic Communications<br>`29` = Veri*factu<br>`30` = BAS<br>`31` = PDF with XML Attachment<br>`32` = FReINV<br>`33` = euBP<br>`34` = ILOI<br>`35` = EDGT<br>`36` = EDCR<br>`37` = NAV |
| 2 | `GenType` | Generation Type | VarChar | 1 | - |  | `N` = Not Relevant<br>`G` = Generate<br>`L` = Generate - Later<br>`F` = Generate - Offline |
| 3 | `MapID` | Electronic Document Format Mapping | Int | 11 | [OLLF](OLLF.md) |  |  |
| 4 | `MapID_WS` | eDoc Web Service Format Mapping | Int | 11 | [OLLF](OLLF.md) |  |  |
| 5 | `TestMode` | Testing Mode Flag | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 6 | `LogInstanc` | Log Instance | Int | 6 | - |  |  |
| 7 | `ParamLogic` | Logic Value Parameter | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `ParamStr` | String Value Parameter | nVarChar | 254 | - |  |  |
| 9 | `ParamLText` | Long Text Parameter | Text | 16 | - |  |  |
| 10 | `ActStatus` | Action Status | VarChar | 1 | - | N | `N` = New<br>`P` = Pending<br>`E` = Error<br>`O` = OK<br>`S` = Sent<br>`R` = Document Error<br>`W` = Waiting<br>`A` = Authorized<br>`I` = In Process<br>`J` = Rejected<br>`D` = Denied<br>`C` = Canceled<br>`B` = Aborted<br>`Q` = Queued<br>`M` = Imported<br>`G` = Warning<br>`o` = Not Approved<br>`e` = Reverse Charge<br>`u` = Continued<br>`f` = Further Objection<br>`a` = Canceling<br>`n` = Continuing<br>`b` = Further Objection in Progress<br>`d` = Resending<br>`w` = Pending to CAEA<br>`k` = Queued<br>`z` = Updating Response |
| 11 | `ParamUqc` | User Query Category | Int | 11 | [OQCN](OQCN.md) |  |  |
| 12 | `ParamInt` | Integer Number | Int | 11 | - |  |  |
| 13 | `ParamPAC` | Authority Code | nVarChar | 16 | [OPAC](OPAC.md) |  |  |
| 14 | `ParamTgl` | Toggle Value Parameter | VarChar | 1 | - |  |  |
| 15 | `ParamMon` | Money Value Parameter (Including Currency) | nVarChar | 254 | - |  |  |
| 16 | `ParamLink` | Hyperlink Parameter | Text | 16 | - |  |  |
| 17 | `Frequency` | Frequency | Int | 11 | - | 1 | `1` = Daily<br>`7` = Weekly<br>`14` = Fortnightly<br>`30` = Monthly<br>`90` = Quarterly |
| 18 | `Source` | Document Source | VarChar | 1 | - | B | `B` = Business Logic<br>`I` = Import |
| 19 | `ReportID` | Report ID | nVarChar | 50 | - |  |  |
| 20 | `AssignedID` | Assigned ID | nVarChar | 50 | - |  |  |
| 21 | `Confirm` | Confirmation | nVarChar | 5 | - |  |  |
| 22 | `PayMethod` | Payment Method | nVarChar | 50 | - | 01 | `01` = Efectivo<br>`02` = Cheque nominativo<br>`03` = Transferencia electr�nica de fondos<br>`04` = Tarjeta de cr�dito<br>`05` = Monedero electr�nico<br>`06` = Dinero electr�nico<br>`08` = Vales de despensa<br>`12` = Daci�n en pago<br>`13` = Pago por subrogaci�n<br>`14` = Pago por consignaci�n<br>`15` = Condonaci�n<br>`17` = Compensaci�n<br>`23` = Novaci�n<br>`24` = Confusi�n<br>`25` = Remisi�n de deuda<br>`26` = Prescripci�n o caducidad<br>`27` = A satisfacci�n del acreedor<br>`28` = Tarjeta de d�bito<br>`29` = Tarjeta de servicios<br>`30` = Aplicaci�n de anticipos<br>`31` = Intermediario pagos<br>`99` = Por definir |
| 23 | `CancStatus` | Cancelation Status | VarChar | 1 | - | T | `T`<br>`N` = New Request<br>`S` = Request Sent<br>`A` = Approved<br>`R` = Rejected<br>`E` = Error<br>`C` = Canceled<br>`I` = In Process<br>`U` = Sent To Authorities<br>`W` = Canceled Without Approval |
| 24 | `CancRecons` | Canceled Reconciliations | nVarChar | 30 | - |  |  |
| 25 | `EntryTypes` | Filter Entry Types | nVarChar | 30 | - |  |  |
| 26 | `EntryStats` | Filter Entry Statuses | nVarChar | 30 | - |  |  |
| 27 | `EntryCncSt` | Filter Entries by Cancellation Status | nVarChar | 30 | - |  |  |
| 28 | `MaxLines` | Filter Max Lines | Int | 6 | - | 0 |  |
| 29 | `BPLId` | Filter Branch ID | Int | 11 | - | -1 |  |
| 30 | `DateFrom` | Filter Date From | Date | 8 | - |  |  |
| 31 | `TimeFrom` | Filter Time From | Int | 11 | - |  |  |
| 32 | `DateTo` | Filter Date To | Date | 8 | - |  |  |
| 33 | `TimeTo` | Filter Time To | Int | 11 | - |  |  |
| 34 | `FromEntry` | Filter From Entry | Int | 11 | - |  |  |
| 35 | `Ascending` | Order Ascending | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 36 | `CodeStr` | Code as a string | nVarChar | 8 | - |  |  |
| 37 | `GUID` | Filter GUID | nVarChar | 100 | - |  |  |
| 38 | `LogType` | Filter Log Type | VarChar | 1 | - | R | INVALID<br>`S` = Send<br>`R` = Receive<br>`I` = Import<br>`N` = Note<br>`W` = Warning<br>`E` = Error<br>`D` = WS Data<br>`B` = Authorities Process Starts<br>`F` = Authorities Process Finished |
| 39 | `LogMessage` | Log Message | Text | 16 | - |  |  |
| 40 | `LogData` | Log Data | Text | 16 | - |  |  |
| 41 | `EDocType` | E-Doc Type | Int | 11 | [OUNCL](OUNCL.md) |  |  |
| 42 | `EDocNum` | E-Doc Number | nVarChar | 100 | - |  |  |
| 43 | `ROText1` | Read Only Text 1 | nVarChar | 254 | - |  |  |
| 44 | `ProcTarget` | Processing Target | nVarChar | 40 | - |  |  |
| 45 | `ParticipID` | E-Doc Number | nVarChar | 128 | - |  |  |
| 46 | `PositMARK` | MARK of Positive Value Invoice | nVarChar | 100 | - |  |  |
| 47 | `NegatMARK` | MARK of Negative Value Invoice | nVarChar | 100 | - |  |  |
| 48 | `EbookRelvt` | Is E-Books Relevant | VarChar | 1 | - |  |  |
| 49 | `PInvType` | Type Abs of Pos. Value Invoice | Int | 11 | [OEIT](OEIT.md) |  |  |
| 50 | `PInvCode` | Type of Pos. Value Invoice | nVarChar | 254 | - |  |  |
| 51 | `NInvType` | Type Abs of Neg. Value Invoice | Int | 11 | [OEIT](OEIT.md) |  |  |
| 52 | `NInvCode` | Type of Neg. Value Invoice | nVarChar | 254 | - |  |  |
| 53 | `BlobCntTyp` | Blob Content Type | Int | 11 | - | -1 | `-1`<br>`0` = XML<br>`1` = Zipped XML<br>`2` = JSON<br>`3` = Zipped JSON<br>`4` = Text |
| 54 | `ZipUnzip` | Zip or Unzip Blob Content | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 55 | `KeepPrefix` | Keep Prefix in Blob Content | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 56 | `DocFunc` | Document Function | VarChar | 1 | - | 0 | `0`<br>`1` = ??? - ????-???????<br>`2` = ?????? - ????-??????? ? o???????<br>`3` = ??? - o???????<br>`4` = ???? - ???????????????? ????-???????<br>`5` = ??????? - ???????????????? ????-??????? ? o???????<br>`6` = ??? - o??????? |
| 57 | `EIRN` | IRN of E-Billing | nVarChar | 254 | - |  |  |
| 58 | `PKP` |  | Text | 16 | - |  |  |
| 59 | `BKP` |  | Text | 16 | - |  |  |
| 60 | `SignMsg` |  | Text | 16 | - |  |  |
| 61 | `SignDigest` |  | Text | 16 | - |  |  |
| 62 | `FechaTimbr` |  | nVarChar | 30 | - |  |  |
| 63 | `SelloSAT` |  | Text | 16 | - |  |  |
| 64 | `RFCofPAC` |  | nVarChar | 100 | - |  |  |
| 65 | `PACSATCert` |  | nVarChar | 100 | - |  |  |
| 66 | `SeqNum` |  | Int | 11 | - |  |  |
| 67 | `SndDateSDI` |  | Date | 8 | - |  |  |
| 68 | `Progressiv` |  | nVarChar | 20 | - |  |  |
| 69 | `ExportFile` |  | Text | 16 | - |  |  |
| 70 | `Descriptn` | Protocol Description | nVarChar | 200 | - |  |  |
| 71 | `CFDiExport` |  | nVarChar | 2 | - | 01 | `01` = No aplica<br>`02` = Definitiva<br>`03` = Temporal<br>`04` = Definitiva con clave distinta a A1 o cuando no existe enajenaci�n en t�rminos del CFF |
| 72 | `TaxProvidr` | Tax Service Provider | nVarChar | 100 | - |  |  |
| 73 | `CancReason` | Cancellation Reason | nVarChar | 2 | - |  |  |
| 74 | `CancResp` | Cancellation Response | nVarChar | 3 | - |  |  |
| 75 | `EBAckNo` | AckNo of E-Billing | nVarChar | 20 | - |  |  |
| 76 | `EBAckDate` | AckDt of E-Billing | nVarChar | 30 | - |  |  |
| 77 | `EBSignINV` | SignedINV of E-Billing | Text | 16 | - |  |  |
| 78 | `EBSignedQC` | SignedQC of E-Billing | Text | 16 | - |  |  |
| 79 | `EBRespSta` | Status of E-Billing | nVarChar | 10 | - |  |  |
| 80 | `FCEID` | FCE ID | nVarChar | 20 | - |  |  |
| 81 | `FCEApprSt` | Approval Status | nVarChar | 30 | - |  |  |
| 82 | `FCEDcApSt` | Doc. Approval Status | nVarChar | 30 | - |  |  |
| 83 | `FCEPaidVal` | Paid Value | nVarChar | 50 | - |  |  |
| 84 | `FCETotalV` | Total Value | nVarChar | 50 | - |  |  |
| 85 | `FCEDocDate` | AFIP Doc. Date | nVarChar | 100 | - |  |  |
| 86 | `FCECBU` | CBU | nVarChar | 254 | - |  |  |
| 87 | `FCEApprDt` | Approval Date | nVarChar | 100 | - |  |  |
| 88 | `FCEDcApDt` | Doc. Approval Date | nVarChar | 100 | - |  |  |
| 89 | `FCEInitAmt` | Initial Amount | nVarChar | 50 | - |  |  |
| 90 | `FCERetent` | Retentions | nVarChar | 50 | - |  |  |
| 91 | `FCEDocRate` | Doc. Exchange Rate | nVarChar | 50 | - |  |  |
| 92 | `CancRef` | Cancellation Reference | nVarChar | 50 | - |  |  |
| 93 | `GenTypeAP` | Generation Type for A/P | VarChar | 1 | - |  | `N` = Not Relevant<br>`G` = Generate<br>`L` = Generate - Later |
| 94 | `AutProcess` | Authorities Process | VarChar | 1 | - |  | None<br>`A` = Approval Process<br>`R` = Rejection Process |
| 95 | `IsEncryptd` | Protocol Encryption Enabled | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 96 | `FEAPInvTyp` | FE-AP Invoice Type | nVarChar | 2 | - | 01 | `01` = Invoice<br>`02` = Debit Memo<br>`03` = Invoice Receipt<br>`04` = Simplified Invoice<br>`05` = Credit Memo |
| 97 | `FEAPOutID` | FE-AP Outbound Financial Doc. ID | nVarChar | 100 | - |  |  |
| 98 | `SttsReason` | Status Reason | nVarChar | 3 | - |  | `NON` = No Issues<br>`REF` = Incorrect references<br>`LEG` = Incorrect legal information<br>`REC` = Unknown receiver<br>`QUA` = Insufficient item quality<br>`DEL` = Issues with delivery<br>`PRI` = Incorrect prices<br>`QTY` = Incorrect quantity<br>`ITM` = Incorrect items<br>`PAY` = Incorrect payment terms<br>`UNR` = Not recognized<br>`FIN` = Incorrect financials<br>`PPD` = Partially Paid<br>`OTH` = Other |
| 99 | `SttsDescr` | Status Description | nVarChar | 254 | - |  |  |
| 100 | `PostPerInv` | Post Per Invoice | VarChar | 1 | - |  |  |
| 101 | `PosiQRPath` | Positive QR Path | nVarChar | 200 | - |  |  |
| 102 | `NegaQRPath` | Negative QR Path | nVarChar | 200 | - |  |  |
| 103 | `CartaPorte` | Complemento Carta Porte ID | nVarChar | 50 | - |  |  |
| 104 | `CartDocTyp` | Carta Porte Document Types | nVarChar | 200 | - |  |  |
| 105 | `CartDocSet` | Apply from Document settings | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 106 | `LogNum` | Log Number | Int | 11 | - |  |  |
| 107 | `C5Relevant` | Corner 5 Relevant | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 108 | `DocUUID` | Document UUID | nVarChar | 128 | - |  |  |
| 109 | `TransUUID` | Transmission UUID | nVarChar | 128 | - |  |  |
| 110 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 111 | `DsptchDate` | Dispatch Date | Date | 8 | - |  |  |
| 112 | `DsptchTime` | Dispatch Time | Int | 11 | - |  |  |
| 113 | `Sensitive` | Value is Sensitive | VarChar | 1 | - |  | `N` = No<br>`Y` = Yes<br>None |
| 114 | `ETypeDesc` | E-Doc Type Description | nVarChar | 254 | - |  |  |
| 115 | `MapIDC5` | Electronic Document Format Mapping C5 | Int | 11 | [OLLF](OLLF.md) |  |  |
| 116 | `CAEA` | CAEA Number | nVarChar | 14 | - |  |  |
| 117 | `CAEAEnable` | CAEA Enabled | VarChar | 1 | - |  |  |
| 118 | `SerialData` | Serialized Data | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code |
