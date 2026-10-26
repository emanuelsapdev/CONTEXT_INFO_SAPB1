# BNK2 - Bank Statement - Recommendation List

- **Tabla:** BNK2
- **Descripción:** Bank Statement - Recommendation List
- **Cantidad de campos:** 29
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/BNK2.html

## Campos (29)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `IdNumber` | Bank Statement ID | Int | 11 | - |  |  |
| 2 | `BSLine` | Bank Statement Line ID | Int | 11 | - |  |  |
| 3 | `ListLineID` | List Line ID | Int | 6 | - |  |  |
| 4 | `DocID` | Document Identifier | nVarChar | 35 | - |  |  |
| 5 | `DocType` | Document Type | Int | 6 | - |  | `15` = Delivery<br>`16` = Returns<br>`203` = A/R Down Payment<br>`13` = A/R Invoice<br>`14` = A/R Credit Memo<br>`132` = Correction Invoice<br>`20` = Goods Receipt PO<br>`21` = Goods Returns<br>`204` = A/P Down Payment<br>`18` = A/P Invoice<br>`19` = A/P Credit Memo<br>`24` = Incoming Payment<br>`25` = Deposit<br>`46` = Payment Advice<br>`57` = Checks for Payment<br>`76` = Postdated Deposit<br>`-2` = Opening Balance<br>`-3` = Closing Balance<br>`30` = Journal Entry<br>`58` = Whse Reconciliation<br>`59` = Goods Receipt<br>`60` = Goods Issue<br>`67` = Inventory Transfers<br>`-1` = All transactions |
| 6 | `AmntLC` | Applied Amount (LC) | Num | 19.6 | - |  |  |
| 7 | `AmntFC` | Applied Amount (FC) | Num | 19.6 | - |  |  |
| 8 | `IsDebit` | Debit [Yes/No] | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 9 | `GLAct` | G/L Account or BP Code | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 10 | `PrftCenter` | Distribution Rule | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 11 | `Project` | Project | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 12 | `VatCode` | VAT Code | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 13 | `Selected` | Selected | VarChar | 1 | - |  | `Y` = Yes<br>`N` = No |
| 14 | `VatLC` | VAT or Discount Amount (LC) | Num | 19.6 | - |  |  |
| 15 | `VatFC` | VAT or Discount Amount (FC) | Num | 19.6 | - |  |  |
| 16 | `Installmnt` | Installment | Int | 11 | - |  |  |
| 17 | `InterimAct` | Interim Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 18 | `JdtLine` | Journal Entry | Int | 11 | [OJDT](OJDT.md) |  |  |
| 19 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 20 | `PrftCent2` | Distribution Rule2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 21 | `PrftCent3` | Distribution Rule3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 22 | `PrftCent4` | Distribution Rule4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 23 | `PrftCent5` | Distribution Rule5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 24 | `MatchLog` | Matching Criteria Log | nVarChar | 254 | - |  |  |
| 25 | `DueBal` | Balance Due | Num | 19.6 | - |  |  |
| 26 | `DueBalFC` | Balance Due (FC) | Num | 19.6 | - |  |  |
| 27 | `AmntSC` | Applied Amount (SC) | Num | 19.6 | - |  |  |
| 28 | `BPLId` | Branch ID | Int | 11 | [OBPL](OBPL.md) |  |  |
| 29 | `BPLName` | Branch Name | nVarChar | 200 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | IdNumber, BSLine, ListLineID |
