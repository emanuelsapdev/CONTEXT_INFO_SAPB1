# DWZ2 - Dunning Wizard Array 2-Invoice Filter

- **Tabla:** DWZ2
- **Descripción:** Dunning Wizard Array 2-Invoice Filter
- **Cantidad de campos:** 43
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DWZ2.html

## Campos (43)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WizardId` | Wizard ID | Int | 11 | [ODWZ](ODWZ.md) |  |  |
| 2 | `CardCode` | BP Card Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 3 | `LetterNum` | Letter Number | Int | 11 | - |  |  |
| 4 | `TotalFee` | Total Fee | Num | 19.6 | - |  |  |
| 5 | `FeeCurr` | Total Fee Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 6 | `TtlopnIntr` | Sum of Open Sum+Interest | Num | 19.6 | - |  |  |
| 7 | `EDunLevel` | Edited Dunning Level | nVarChar | 3 | - |  |  |
| 8 | `OpnIntrCrr` | Total Open + Interest Currency | nVarChar | 3 | - |  |  |
| 9 | `DocAbs` | Document Internal Number | Int | 11 | - |  |  |
| 10 | `DocNum` | Doc. No. | Int | 11 | - |  |  |
| 11 | `InstlmntID` | Installment ID | Int | 6 | - |  |  |
| 12 | `IntrstPC` | Interest Percent | Num | 19.6 | - |  |  |
| 13 | `IntrstAmnt` | Interest Amount | Num | 19.6 | - |  |  |
| 14 | `IntrstCurr` | Interest Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 15 | `ChckLine` | Checked Row | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 16 | `IntrstDays` | Interest Days | Int | 11 | - |  |  |
| 17 | `DocType` | Source Table | Int | 11 | - |  | `13` = A/R Invoice<br>`203` = Down Payment Incoming<br>`165` = Correction A/R Invoice<br>`14` = A/R Credit Memo<br>`24` = Incoming Payment<br>`30` = Journal Transactions<br>`-2` = Open Balance<br>`-3` = Close Balance<br>`46` = Outgoing Payments |
| 18 | `DueDate` | Due Date | Date | 8 | - |  |  |
| 19 | `LetterLvl` | Letter Level | nVarChar | 3 | - | 0 |  |
| 20 | `OpenSum` | Open Sum | Num | 19.6 | - |  |  |
| 21 | `OpenCurr` | Open Sum Currency | nVarChar | 3 | - |  |  |
| 22 | `sumIntrClc` | Sum for Interest Calculation | Num | 19.6 | - |  |  |
| 23 | `folioNum` | Folio Number | nVarChar | 14 | - |  |  |
| 24 | `LvlUpdated` | Level Updated Flag | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 25 | `TotalFeeFC` | Total Fee in Document Currency | Num | 19.6 | - |  |  |
| 26 | `TotalFeeLC` | Total Fee in Local Currency | Num | 19.6 | - |  |  |
| 27 | `TotalFeeSC` | Total Fee in System Currency | Num | 19.6 | - |  |  |
| 28 | `TtlopnInFC` | Sum of Open Sum+Interest FC | Num | 19.6 | - |  |  |
| 29 | `TtlopnInSC` | Sum of Open Sum+Interest SC | Num | 19.6 | - |  |  |
| 30 | `IntrAmtFC` | Interest Amount (FC) | Num | 19.6 | - |  |  |
| 31 | `IntrAmtSC` | Interest Amount (SC) | Num | 19.6 | - |  |  |
| 32 | `OpenSumFC` | Open Sum (FC) | Num | 19.6 | - |  |  |
| 33 | `OpenSumSC` | Open Sum (SC) | Num | 19.6 | - |  |  |
| 34 | `ExeChkLine` | Executed Checked Row | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 35 | `AutoPost` | Automatic Posting | VarChar | 1 | - | N | `N` = No<br>`B` = Interest and Fee<br>`I` = Interest Only<br>`F` = Fee Only |
| 36 | `DocRate` | Document Rate | Num | 19.6 | - |  |  |
| 37 | `UnpaidBoEV` | Unpaid BoE Value | Num | 19.6 | - |  |  |
| 38 | `BoENumber` | BoE Number | Int | 11 | - |  |  |
| 39 | `BoEStatus` | BoE Status | VarChar | 1 | - |  |  |
| 40 | `BoEDate` | BoE Date | Date | 8 | - |  |  |
| 41 | `BoEKey` | BoE Key | Int | 11 | - |  |  |
| 42 | `BPType` | Business Partner Type | VarChar | 1 | - | C | `C` = Customer<br>`S` = Vendor |
| 43 | `BPLId` | Assigned Branch | Int | 11 | [OBPL](OBPL.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WizardId, LetterNum, DocAbs, InstlmntID, DocType |
