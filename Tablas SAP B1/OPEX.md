# OPEX - Payment Results Table

- **Tabla:** OPEX
- **Descripción:** Payment Results Table
- **Cantidad de campos:** 140
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OPEX.html

## Campos (140)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `PayRunDate` | Date of Payment Run | Date | 8 | - |  |  |
| 3 | `VendorNum` | Vendor Code | nVarChar | 15 | - |  |  |
| 4 | `CustNum` | Customer Code | nVarChar | 15 | - |  |  |
| 5 | `PaymMethod` | Payment Means | nVarChar | 15 | - |  |  |
| 6 | `PaymDocNum` | Payment Document No. | Int | 11 | - |  |  |
| 7 | `FiscalYear` | Fiscal Year | Date | 8 | - |  |  |
| 8 | `Country` | Company Country/Region | nVarChar | 3 | - |  |  |
| 9 | `CompTaxNum` | Company Tax Number | nVarChar | 32 | - |  |  |
| 10 | `PayeeName` | Payee Name | nVarChar | 200 | - |  |  |
| 11 | `PayeeZip` | Payee Zip Code | nVarChar | 20 | - |  |  |
| 12 | `PayeeCity` | Payee City | nVarChar | 100 | - |  |  |
| 13 | `PayeeStree` | Payee Street | nVarChar | 100 | - |  |  |
| 14 | `PayCountry` | Payee Country/Region | nVarChar | 3 | - |  |  |
| 15 | `PayeeState` | Payee State | nVarChar | 3 | - |  |  |
| 16 | `PayBnkName` | Payee Bank Name | nVarChar | 250 | - |  |  |
| 17 | `PayBankZip` | Payee Bank Zip Code | nVarChar | 20 | - |  |  |
| 18 | `PayBnkCity` | Payee Bank City | nVarChar | 100 | - |  |  |
| 19 | `PayBnkStr` | Payee Bank Street | nVarChar | 100 | - |  |  |
| 20 | `PayBnkCntr` | Payee Bank Country/Region | nVarChar | 3 | - |  |  |
| 21 | `PayBankAct` | Payee Bank Account | nVarChar | 50 | - |  |  |
| 22 | `PayBnkCode` | Payee Bank Code | nVarChar | 30 | - |  |  |
| 23 | `PayBnkCtrl` | Payee Bank Control Number | nVarChar | 2 | - |  |  |
| 24 | `PayBnkSwif` | Payee Bank BIC/SWIFT Code | nVarChar | 50 | - |  |  |
| 25 | `PayBnkIBAN` | Payee Bank IBAN | nVarChar | 50 | - |  |  |
| 26 | `PymPostDat` | Payment Posting Date | Date | 8 | - |  |  |
| 27 | `PymBnkAcct` | Payment Bank Account | nVarChar | 50 | - |  |  |
| 28 | `PymBnkCntr` | Payment Bank Country/Region | nVarChar | 3 | - |  |  |
| 29 | `PymBnkCode` | Payment Bank Code | nVarChar | 30 | - |  |  |
| 30 | `PymBnkIBAN` | Payment Bank IBAN | nVarChar | 50 | - |  |  |
| 31 | `PymGLAcct` | Payment G/L Account | nVarChar | 15 | - |  |  |
| 32 | `Currency` | Main Currency | nVarChar | 3 | - |  |  |
| 33 | `PymDocAmnt` | Payment Document Amount (LC) | Num | 19.6 | - |  |  |
| 34 | `PymDocCurr` | Payment Document Currency | nVarChar | 3 | - |  |  |
| 35 | `PymDcAmtFC` | Payment Document Amount (FC) | Num | 19.6 | - |  |  |
| 36 | `PymCshDsct` | Cash Discount in Payment Doc | Num | 19.6 | - |  |  |
| 37 | `PyCshDscFC` | Cash Discount in Payment Doc | Num | 19.6 | - |  |  |
| 38 | `PymNumOfPa` | Number of Items Paid | Int | 11 | - |  |  |
| 39 | `PymDocRate` | Payment Document Exchange Rate | Num | 19.6 | - |  |  |
| 40 | `Status` | Status | VarChar | 1 | - | O | `O` = Open<br>`C` = Closed |
| 41 | `PaymWizCod` | Payment Wizard Code | Int | 11 | [OPWZ](OPWZ.md) |  |  |
| 42 | `InstrucKey` | Instruction Key | nVarChar | 30 | - |  |  |
| 43 | `CllctAutho` | Collection Authorization | VarChar | 1 | - |  |  |
| 44 | `PayBnkPost` | Payee Bank Post Office | VarChar | 1 | - |  |  |
| 45 | `PayBnkChNo` | Payee Bank Next Check No. | Int | 11 | - |  |  |
| 46 | `PayBnkHsBk` | Payee Bank House Bank | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 47 | `PayBnkBlck` | Payee Bank Block | nVarChar | 100 | - |  |  |
| 48 | `PayBnkCnty` | Payee Bank County | nVarChar | 100 | - |  |  |
| 49 | `PayBnkStat` | Payee Bank State | nVarChar | 3 | - |  |  |
| 50 | `PayBnkBISR` | Payee Bank BISR | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 51 | `PayBnkUsr1` | Payee Bank User No. 1 | nVarChar | 25 | - |  |  |
| 52 | `PayBnkUsr2` | Payee Bank User No. 2 | nVarChar | 25 | - |  |  |
| 53 | `PayBnkUsr3` | Payee Bank User No. 3 | nVarChar | 25 | - |  |  |
| 54 | `PayBnkUsr4` | Payee Bank User No. 4 | nVarChar | 25 | - |  |  |
| 55 | `PaymFormat` | Payment Format | nVarChar | 20 | - |  |  |
| 56 | `CompName` | Company Name | nVarChar | 200 | - |  |  |
| 57 | `CompAddres` | Company Address | nVarChar | 254 | - |  |  |
| 58 | `CompISRBil` | Company ISR Biller ID | nVarChar | 9 | - |  |  |
| 59 | `VendISRBil` | Vendor ISR Biller ID | nVarChar | 9 | - |  |  |
| 60 | `AddIdNum` | Additional ID No. | nVarChar | 32 | - |  |  |
| 61 | `CompOrgNum` | Company Organization No. | nVarChar | 100 | - |  |  |
| 62 | `PayBnkBrnc` | Payee Bank Branch | nVarChar | 50 | - |  |  |
| 63 | `PymBnkBrnc` | Payment Bank Branch | nVarChar | 50 | - |  |  |
| 64 | `UserName` | User Name | nVarChar | 155 | - |  |  |
| 65 | `UserEmail` | User E-Mail | nVarChar | 100 | - |  |  |
| 66 | `UserPortNo` | User Mobile Phone No. | nVarChar | 50 | - |  |  |
| 67 | `UserFax` | User Fax No. | nVarChar | 50 | - |  |  |
| 68 | `Department` | User Department | Int | 6 | - |  |  |
| 69 | `DebitMemo` | Debit Memo | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 70 | `EuInTrnsfr` | EU Internal Transfer | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 71 | `FilePath` | File Path | Text | 16 | - |  |  |
| 72 | `OrderParty` | Ordering Party | nVarChar | 30 | - |  |  |
| 73 | `PymCtrlKey` | Payment Bank Control Number | nVarChar | 2 | - |  |  |
| 74 | `PayeeTaxNo` | Payee Tax Number | nVarChar | 32 | - |  |  |
| 75 | `PymKeyCode` | Payment Key Code | nVarChar | 6 | - |  |  |
| 76 | `PayRefDtls` | Payee Reference Details | nVarChar | 20 | - |  |  |
| 77 | `FormatName` | Format Name | nVarChar | 100 | - |  |  |
| 78 | `CheckPmnt` | Payment Done with Check | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 79 | `PymBnkUsr1` | Payment Bank User No. 1 | nVarChar | 25 | - |  |  |
| 80 | `PymBnkUsr2` | Payment Bank User No. 2 | nVarChar | 25 | - |  |  |
| 81 | `PymBnkUsr3` | Payment Bank User No. 3 | nVarChar | 25 | - |  |  |
| 82 | `PymBnkUsr4` | Payment Bank User No. 4 | nVarChar | 25 | - |  |  |
| 83 | `CompStreet` | Company Street | nVarChar | 100 | - |  |  |
| 84 | `CompBlock` | Company Block | nVarChar | 100 | - |  |  |
| 85 | `CompCity` | Company City | nVarChar | 100 | - |  |  |
| 86 | `CompZip` | Company Zip Code | nVarChar | 20 | - |  |  |
| 87 | `CompCounty` | Company County | nVarChar | 100 | - |  |  |
| 88 | `CompState` | Company State | nVarChar | 3 | [OCST](OCST.md) |  |  |
| 89 | `PymBCACode` | Payment Bank Charges | nVarChar | 3 | [OBCA](OBCA.md) |  |  |
| 90 | `PaymDocTyp` | Payment Document Object Type | nVarChar | 20 | - |  |  |
| 91 | `PayOrderNo` | Payment Order Number | Int | 11 | [OIPO](OIPO.md) |  |  |
| 92 | `FreeText1` | Free Text 1 | nVarChar | 254 | - |  |  |
| 93 | `FreeText2` | Free Text 2 | nVarChar | 254 | - |  |  |
| 94 | `FreeText3` | Free Text 3 | nVarChar | 254 | - |  |  |
| 95 | `PymBnkSwif` | Payment Bank Swift Code | nVarChar | 50 | - |  |  |
| 96 | `PayBnkUIC` | Payee Bank UIC Code | nVarChar | 3 | - |  |  |
| 97 | `LineType` | Line Type | VarChar | 1 | - | G | `G` = General<br>`O` = Pay on Account<br>`T` = Pay to Account |
| 98 | `BoeKey` | Bill of Exchange Key | Int | 11 | [OBOE](OBOE.md) |  |  |
| 99 | `BoeCurrSta` | BoE Current Status | VarChar | 1 | - |  |  |
| 100 | `BoeDate` | Bill of Exchange Date | Date | 8 | - |  |  |
| 101 | `BoeDueDate` | BoE Due Date | Date | 8 | - |  |  |
| 102 | `Instruct1` | BoE Instruction 1 | nVarChar | 2 | - |  |  |
| 103 | `Instruct2` | BoE Instruction 2 | nVarChar | 2 | - |  |  |
| 104 | `BoeCancIns` | BoE Cancel Instruction | nVarChar | 2 | - |  |  |
| 105 | `BoeOccCode` | BoE Occurrence Code | nVarChar | 2 | - |  |  |
| 106 | `BoePtfID` | BoE Internal Portfolio ID | nVarChar | 3 | - |  |  |
| 107 | `BoeOurNum` | Our Number in Next BoE | Int | 11 | - |  |  |
| 108 | `BoeIntrAm` | BoE Interest Amount | Num | 19.6 | - |  |  |
| 109 | `BoeDiscD` | BoE Discount Date | Date | 8 | - |  |  |
| 110 | `BoeDisAmnt` | BoE Discount Amount | Num | 19.6 | - |  |  |
| 111 | `BoeFineD` | BoE Fine Date | Date | 8 | - |  |  |
| 112 | `BoeFineAmt` | BoE Fine Amount | Num | 19.6 | - |  |  |
| 113 | `BoeIntrstD` | BoE Interest Date | Date | 8 | - |  |  |
| 114 | `BoeIOFAmt` | BoE IOF Amount | Num | 19.6 | - |  |  |
| 115 | `BoeMovCode` | BoE Movement Code | nVarChar | 10 | - |  |  |
| 116 | `BarcodeRep` | Barcode Representation | nVarChar | 100 | - |  |  |
| 117 | `PONumber` | External Payment Order Number | Int | 11 | - |  |  |
| 118 | `POSeries` | External Payment Order Series | Int | 11 | - |  |  |
| 119 | `PaPriority` | Payment Priority | VarChar | 1 | - | 6 | `1`<br>`2`<br>`3`<br>`4`<br>`5`<br>`6` |
| 120 | `PaymType` | Payment Type | VarChar | 1 | - | N | `N`<br>`E` = Electronic<br>`P` = Mail<br>`T` = Telegraph<br>`X` = Express |
| 121 | `RecipStatu` | Recipient Status | nVarChar | 2 | - |  |  |
| 122 | `BudegetId` | VAT Budget Classification Code | nVarChar | 100 | - |  |  |
| 123 | `OKATO` | OKATO | nVarChar | 11 | - |  |  |
| 124 | `PymReason` | Payment Reason | nVarChar | 2 | - |  |  |
| 125 | `PostPeriod` | Posting Period Code | nVarChar | 10 | - |  |  |
| 126 | `BaseDocTyp` | Base Document Type | nVarChar | 2 | - |  |  |
| 127 | `BaseDocDat` | Base Document Date | Date | 8 | - |  |  |
| 128 | `TaxPymType` | Tax Payment Type | nVarChar | 2 | - |  |  |
| 129 | `OKTMO` | OKTMO | nVarChar | 12 | - |  |  |
| 130 | `SeqType` | Sequence Type | nVarChar | 4 | - |  | `OOFF` = OOFF<br>`FRST` = FRST<br>`RCUR` = RCUR<br>`FNAL` = FNAL |
| 131 | `PymDate` | Payment Date | Date | 8 | - |  |  |
| 132 | `PymBnkName` | Payment Bank Name | nVarChar | 250 | - |  |  |
| 133 | `UIPCode` | UIP Code | nVarChar | 25 | - |  |  |
| 134 | `UserId` | User ID | Int | 6 | [OUSR](OUSR.md) |  |  |
| 135 | `SpltPmtVAT` | Split Payment | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 136 | `EnBnkAct` | Encryption of Payee Bank Acct | Text | 16 | - |  |  |
| 137 | `EnBnkIBan` | Encryption of Payee Bank IBAN | Text | 16 | - |  |  |
| 138 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |
| 139 | `DPPStatus` | Data Protection Status | VarChar | 1 | - | N | `N` = None<br>`D` = Erased |
| 140 | `EnPmBnkAct` | Encryption of Payment Bank Account | Text | 16 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
