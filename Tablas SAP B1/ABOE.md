# ABOE - Bill of Exchange for Payment - History

- **Tabla:** ABOE
- **Descripción:** Bill of Exchange for Payment - History
- **Cantidad de campos:** 93
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ABOE.html

## Campos (93)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `BoeKey` | Bill of Exchange Key | Int | 11 | - |  |  |
| 2 | `BoeNum` | Bill of Exchange No. | Int | 11 | - |  |  |
| 3 | `BoeStatus` | Bill of Exchange Status | VarChar | 1 | - |  | `G` = Generated<br>`S` = Sent<br>`D` = Deposited<br>`P` = Paid<br>`C` = Canceled<br>`L` = Closed<br>`F` = Failed<br>`V` = BoE to Vendor |
| 4 | `BoeType` | Bill of Exchange Type | VarChar | 1 | - | I | `I` = Incoming<br>`O` = Outgoing |
| 5 | `DpsBankCod` | Deposit Bank Code | nVarChar | 30 | - |  |  |
| 6 | `DpsCntrCod` | Deposit Country/Region Code | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 7 | `DueDate` | Bill of Exchange Due Date | Date | 8 | - |  |  |
| 8 | `DpstAcct` | Bank Account No. | nVarChar | 50 | - |  |  |
| 9 | `DpstBranch` | Branch for Payments | nVarChar | 50 | - |  |  |
| 10 | `Details` | Details | nVarChar | 50 | - |  |  |
| 11 | `TransRef` | Journal Entry Reference | nVarChar | 8 | - |  |  |
| 12 | `PmntDate` | Payment Date | Date | 8 | - |  |  |
| 13 | `PmntNum` | Payment No. | Int | 11 | - |  |  |
| 14 | `BoeSum` | Bill of Exchange Amount | Num | 19.6 | - |  |  |
| 15 | `BoeSumSC` | Bill of Exchange Amount (SC) | Num | 19.6 | - |  |  |
| 16 | `BoeSumFC` | Bill of Exchange Amount (FC) | Num | 19.6 | - |  |  |
| 17 | `CardCode` | BP Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 18 | `CardName` | BP Name | nVarChar | 200 | - |  |  |
| 19 | `BoeAcct` | BP Account Code | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 20 | `Currency` | Bill of Exchange Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 21 | `Printed` | Printed | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 22 | `TotalWords` | Total in Words | nVarChar | 100 | - |  |  |
| 23 | `Signature` | Signature | nVarChar | 155 | - |  |  |
| 24 | `TransNum` | Transaction No. | Int | 11 | - | 0 |  |
| 25 | `LinesSum` | Row Totals | Num | 19.6 | - |  |  |
| 26 | `DdctPrcnt` | % Withholding Tax Ded. | Num | 19.6 | - |  |  |
| 27 | `Address` | Address | nVarChar | 254 | - |  |  |
| 28 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 29 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 30 | `VatTotal` | Total Tax | Num | 19.6 | - |  |  |
| 31 | `VatTotalSC` | Total Tax (SC) | Num | 19.6 | - |  |  |
| 32 | `VatTotalFC` | Total Tax (FC) | Num | 19.6 | - |  |  |
| 33 | `VatCalcult` | Calculate Tax | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 34 | `TaxDate` | Document Date | Date | 8 | - |  |  |
| 35 | `DataSource` | Data Source | VarChar | 1 | - | N | `N` = Unknown<br>`I` = Interface<br>`U` = Upgrade<br>`M` = Import<br>`O` = DI API<br>`S` = Service Layer<br>`W` = Web Client<br>`A` = Doc. Generation Wizard<br>`D` = Restore Wizard<br>`P` = Partner Implementation<br>`T` = Year Transfer |
| 36 | `SumRfndCln` | Deduction Refund Amount | Num | 19.6 | - |  |  |
| 37 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 38 | `PrintedBy` | Printed By | Int | 6 | - |  |  |
| 39 | `Transfered` | Transferred to next year | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 40 | `Instance` | Instance | Int | 6 | - | 0 |  |
| 41 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 42 | `BPBankCod` | BP Bank Code | nVarChar | 30 | - |  |  |
| 43 | `BPBankNam` | BP Bank Name | nVarChar | 250 | - |  |  |
| 44 | `BPBankAct` | BP Bank Account | nVarChar | 50 | - |  |  |
| 45 | `BPBankBrnc` | BP Bank Branch | nVarChar | 50 | - |  |  |
| 46 | `BPBankCtr` | BP Bank Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 47 | `RefNum` | Reference No. | nVarChar | 254 | - |  |  |
| 48 | `IsReconcld` | Reconciled | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 49 | `Comments` | Remarks | nVarChar | 254 | - |  |  |
| 50 | `PayMethCod` | Payment Method Code | nVarChar | 15 | [OPYM](OPYM.md) |  |  |
| 51 | `DepositNum` | Deposit Number | Int | 11 | - |  |  |
| 52 | `PymMethNam` | Payment Method Name | nVarChar | 100 | - |  |  |
| 53 | `DeductSum` | Deduction Amount | Num | 19.6 | - |  |  |
| 54 | `ControlKey` | Control Key | nVarChar | 2 | - |  |  |
| 55 | `AgentCode` | Agent Code | nVarChar | 32 | [OAGP](OAGP.md) |  |  |
| 56 | `ReconcilNu` | External Reconciliation No. | Int | 11 | - |  |  |
| 57 | `DepositTyp` | Deposit Type | VarChar | 1 | - |  | `C` = Collection<br>`D` = Discounted |
| 58 | `CreatStatu` | Creation Status | VarChar | 1 | - |  | `G` = Generated<br>`S` = Sent |
| 59 | `Ref2` | Reference 2 | nVarChar | 254 | - |  |  |
| 60 | `PayEngSt1` | Payment Engine Status 1 | VarChar | 1 | - |  |  |
| 61 | `PayEngSt2` | Payment Engine Status 2 | VarChar | 1 | - |  |  |
| 62 | `PayEngSt3` | Payment Engine Status 3 | nVarChar | 3 | - |  |  |
| 63 | `StampTax` | Stamp Tax Code | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 64 | `StmpTxAmnt` | Stamp Tax Amount | Num | 19.6 | - |  |  |
| 65 | `DpsActKey` | Bank Account Internal ID | Int | 11 | [DSC1](DSC1.md) |  |  |
| 66 | `OutBnkKey` | Outgoing Bank Account Key | Int | 11 | [DSC1](DSC1.md) |  |  |
| 67 | `Portfolio` | Portfolio | nVarChar | 8 | [OPFT](OPFT.md) |  |  |
| 68 | `VndCodeCEE` | Vendor Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 69 | `VndNameCEE` | Vendor Name | nVarChar | 200 | - |  |  |
| 70 | `OurNum` | Our Number | Int | 11 | - |  |  |
| 71 | `BarcodeNum` | Bar Code Number | nVarChar | 120 | - |  |  |
| 72 | `BarcodeRep` | Bar Code Representation | nVarChar | 100 | - |  |  |
| 73 | `OurNumChk` | Our Number Check Digit | VarChar | 1 | - |  |  |
| 74 | `FolioPref` | Folio Prefix String | nVarChar | 4 | - |  |  |
| 75 | `FolioNum` | Folio Number | Int | 11 | - |  |  |
| 76 | `LPgFolioN` | Folio No. for Last Page in Doc. | Int | 11 | - |  |  |
| 77 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 78 | `IntrstAmnt` | Interest Amount | Num | 19.6 | - |  |  |
| 79 | `DiscAmnt` | Discount Amount | Num | 19.6 | - |  |  |
| 80 | `FineAmnt` | Fine Amount | Num | 19.6 | - |  |  |
| 81 | `IntrstDate` | BoE Interest Date | Date | 8 | - |  |  |
| 82 | `DiscDate` | BoE Discount Date | Date | 8 | - |  |  |
| 83 | `FineDate` | BoE Fine Date | Date | 8 | - |  |  |
| 84 | `PostType` | Posting Type | VarChar | 1 | - |  | `D` = Default<br>`A` = Alternative |
| 85 | `IOFAmnt` | IOF Amount | Num | 19.6 | - |  |  |
| 86 | `ServFeeAm` | Service Fee Amount | Num | 19.6 | - |  |  |
| 87 | `OtherExAm` | Other Expenses Amount | Num | 19.6 | - |  |  |
| 88 | `OtherInAm` | Other Incomes Amount | Num | 19.6 | - |  |  |
| 89 | `BPLId` | Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 90 | `EnBPBnkAct` | Encryption of BP Bank Account | Text | 16 | - |  |  |
| 91 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 92 | `DPPStatus` | Data Protection Status | VarChar | 1 | - | N | `N` = None<br>`D` = Erased |
| 93 | `EnDpstAcct` | Encryption of Bank Account No. | Text | 16 | - |  |  |

## Claves e índices (5)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | BoeKey, LogInstanc |
| VPM_NUM | No | PmntNum |
| TRANS_NUM | No | TransNum |
| DPS_NUM | No | DepositNum |
| BOE_NUM | Yes | BoeNum, BoeType, LogInstanc |
