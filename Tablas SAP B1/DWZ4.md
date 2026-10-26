# DWZ4 - Dunning Wizard Array 4-Paging Grid

- **Tabla:** DWZ4
- **Descripción:** Dunning Wizard Array 4-Paging Grid
- **Cantidad de campos:** 51
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/DWZ4.html

## Campos (51)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WizardId` | Wizard ID | Int | 11 | [ODWZ](ODWZ.md) |  |  |
| 2 | `CheckLine` | Checked Row | VarChar | 1 | - | Y |  |
| 3 | `ExeChkLine` | Executed Checked Row | VarChar | 1 | - | Y |  |
| 4 | `RowId` | Row Num | Int | 11 | - |  |  |
| 5 | `CardCode` | BP Card Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 6 | `LetterNum` | Letter Number | Int | 11 | - |  |  |
| 7 | `DunnLevel` | Dunning Level | Int | 11 | - |  |  |
| 8 | `CardName` | BP Name | nVarChar | 200 | - |  |  |
| 9 | `DocCur` | Doc. Currency | nVarChar | 3 | - |  |  |
| 10 | `DocType` | Source Table | Int | 11 | - |  | `13` = A/R Invoice<br>`203` = Down Payment Incoming<br>`165` = Correction A/R Invoice<br>`14` = A/R Credit Memo<br>`24` = Incoming Payment<br>`30` = Journal Transactions<br>`-2` = Open Balance<br>`-3` = Close Balance |
| 11 | `DocNum` | Doc. No. | Int | 11 | - |  |  |
| 12 | `InstlmntID` | Installment ID | Int | 6 | - |  |  |
| 13 | `DueDate` | Due Date | Date | 8 | - |  |  |
| 14 | `LastLvlDte` | Last Update Date | Date | 8 | - |  |  |
| 15 | `LastDunDte` | Last Dunning Date | Date | 8 | - |  |  |
| 16 | `NewLvlDate` | New Level Update Date | Date | 8 | - |  |  |
| 17 | `DocAmntLC` | DOC. AMOUNT (LC) | nVarChar | 100 | - |  |  |
| 18 | `DocAmntFC` | DOC. AMOUNT (FC) | nVarChar | 100 | - |  |  |
| 19 | `OpenAmtLC` | Open Amount (LC) | nVarChar | 100 | - |  |  |
| 20 | `OpenAmtFC` | Open Amount (FC) | nVarChar | 100 | - |  |  |
| 21 | `IntrstDays` | Interest Days | Int | 11 | - |  |  |
| 22 | `IntrstPC` | Interest Percent | Num | 19.6 | - |  |  |
| 23 | `IntAmntLC` | Interest Amount (LC) | nVarChar | 100 | - |  |  |
| 24 | `IntAmntFC` | Interest Amount (FC) | nVarChar | 100 | - |  |  |
| 25 | `InclAmntLC` | Total Incl. Amount (LC) | nVarChar | 100 | - |  |  |
| 26 | `InclAmntFC` | Total Incl. Amount (FC) | nVarChar | 100 | - |  |  |
| 27 | `FeeLC` | Fee (LC) | nVarChar | 100 | - |  |  |
| 28 | `FeeFC` | Fee (FC) | nVarChar | 100 | - |  |  |
| 29 | `AllTotalLC` | Overall Total (LC) | nVarChar | 100 | - |  |  |
| 30 | `AllTotalFC` | Overall Total (FC) | nVarChar | 100 | - |  |  |
| 31 | `AutoPost` | Automatic Posting | VarChar | 1 | - | N | `N` = No<br>`B` = Interest and Fee<br>`I` = Interest Only<br>`F` = Fee Only |
| 32 | `LineProp` | Line Property | Int | 11 | - |  |  |
| 33 | `YearDays` | Year Days | Int | 11 | - |  |  |
| 34 | `YearlyRate` | Yearly Rate | Num | 19.6 | - |  |  |
| 35 | `LetterFrmt` | Letter Formant | nVarChar | 8 | - |  |  |
| 36 | `MinBlan` | Min. Balance | Num | 19.6 | - |  |  |
| 37 | `GrpMethod` | Group Method | VarChar | 1 | - |  |  |
| 38 | `DocEntry` | DocEntry | Int | 11 | - |  |  |
| 39 | `DocRate` | Exchange Rate on Document | nVarChar | 100 | - |  |  |
| 40 | `FeeCurr` | Fee Currency | nVarChar | 3 | - |  |  |
| 41 | `OrigFee` | Original Fee on Dunning Term | Num | 19.6 | - |  |  |
| 42 | `MinBalCurr` | Minimum Balance Currency | nVarChar | 3 | - |  |  |
| 43 | `LvlUpdated` | Level Updated | nVarChar | 3 | - |  |  |
| 44 | `DunAddr` | Dunning Address | nVarChar | 254 | - |  |  |
| 45 | `DocText` | Doc. Text | nVarChar | 254 | - |  |  |
| 46 | `ParentId` | Parent Id | Int | 11 | - |  |  |
| 47 | `BpCode2` | BP Code 2 | nVarChar | 15 | - |  |  |
| 48 | `BpType` | BP Type | VarChar | 1 | - |  |  |
| 49 | `CardName2` | Card Name 2 | nVarChar | 200 | - |  |  |
| 50 | `Comment` | Comment | nVarChar | 254 | - |  |  |
| 51 | `BPLId` | Branch ID | Int | 11 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WizardId, RowId |
