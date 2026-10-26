# CASE1 - Internal Recon. Upgrade 2007A

- **Tabla:** CASE1
- **Descripción:** Internal Recon. Upgrade 2007A
- **Cantidad de campos:** 36
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/CASE1.html

## Campos (36)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Header Internal ID | Int | 11 | [CASE](CASE.md) |  |  |
| 2 | `LineId` | Inconsistent Amt Number | Int | 11 | - | 0 |  |
| 3 | `ShortName` | BP Code | nVarChar | 15 | - |  |  |
| 4 | `Account` | Account Code | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 5 | `OrigAbsEnt` | Original Doc. Internal ID | Int | 11 | - |  |  |
| 6 | `OrigObjTyp` | Original Doc. Type | Int | 11 | - | 0 | `0` = All<br>`13` = A/R Invoice<br>`14` = A/R Credit Memo<br>`18` = A/P Invoice<br>`19` = A/P Credit Memo<br>`24` = Incoming Payment<br>`30` = Journal Entry<br>`46` = Outgoing Payment<br>`163` = A/P Correction Invoice<br>`165` = A/R Correction Invoice<br>`203` = A/R Down Payment<br>`204` = A/P Down Payment |
| 7 | `OrigDocNum` | Original Document Number | Int | 11 | - |  |  |
| 8 | `OrigInsNum` | Original Installment Number | Int | 11 | - |  |  |
| 9 | `OrigTrnsId` | Original JE Trans. No. | Int | 11 | [OJDT](OJDT.md) |  |  |
| 10 | `OrigTrnsLn` | Original JE Row No. | Int | 11 | - |  |  |
| 11 | `LnkRecnAbs` | Linked Recon. Doc. Internal ID | Int | 11 | - |  |  |
| 12 | `LnkRecnObj` | Destination Object Type | Int | 11 | - |  |  |
| 13 | `LnkRecnNum` | Destination Document Number | Int | 11 | - |  |  |
| 14 | `LnkRecnIns` | Destination Installment Number | Int | 11 | - |  |  |
| 15 | `LnkRecnTrn` | Linked and Recon. JE Trans No. | Int | 11 | [OJDT](OJDT.md) |  |  |
| 16 | `LnkRecnLn` | Linked and Recon. JE Row No. | Int | 11 | - |  |  |
| 17 | `InconsType` | Type of Inconsistency | nVarChar | 2 | - |  | `1` = Invoice Linked to Reconciled Payment<br>`2` = Credit Memo Linked to Reconciled Payment<br>`3` = Canceled Reconciliation<br>`4` = Partial Exchange Rate Difference Recognition<br>`5` = Payment Linked to Reconciled Transaction<br>`6` = Journal Entry Linked to Reconciled Payment<br>`7` = Unbalanced Reconciliation<br>`8` = Invoice/Credit Linked to Credit/Invoice<br>`9` = Balancing Upgrade Journal Transaction<br>`10` = Canceled Payment or Journal Entry<br>`11` = Cancellation of Payment/JE within Payment<br>`12` = Unreconciled Balance Rows in Multiple BPs Reconciliation<br>`13` = Missing Exchange Rate Difference behind Multiple BPs Reconciliation<br>`14` = Double Application of Payments of Down Payment Request<br>`15` = Exchange Difference Recognition of Payments of DPM Requests<br>`16` = Reconciliation of Payments Associated with DPM Request<br>`17` = Unbalanced Multiple BP Reconciliation<br>`18` = Amount Differences<br>`19` = Double application of invoice after linking of down payment<br>`20` = Canceled payment of down payment request<br>`21` = Credit Memo based on a Year Transfered invoice<br>`22` = Payment of a year transfer document<br>`23` = Processing of Payment Linked to Transactions<br>`24` = Consolidating Business Partner<br>`25` = Multiple Control Accounts<br>`26` = Different Control Accounts in a Canceled Payment<br>`0` = None |
| 18 | `ReconNum` | Reconciliation Number | Int | 11 | - |  |  |
| 19 | `NewRcnNum` | New Reconciliation No. | Int | 11 | [OITR](OITR.md) |  |  |
| 20 | `CredDeb` | Credit or Debit | VarChar | 1 | - |  |  |
| 21 | `Amount` | Inconsistent Amount | Num | 19.6 | - |  |  |
| 22 | `AmountFC` | Inconsistent Amount (FC) | Num | 19.6 | - |  |  |
| 23 | `AmountSC` | Inconsistent Amount (SC) | Num | 19.6 | - |  |  |
| 24 | `TransId` | Balancing Trans. Internal ID | Int | 11 | [OJDT](OJDT.md) |  |  |
| 25 | `TransLine` | Balancing Transaction Row No. | Int | 11 | - |  |  |
| 26 | `X` | x | Num | 19.6 | - |  |  |
| 27 | `Y` | Y | Num | 19.6 | - |  |  |
| 28 | `Z` | Z | Num | 19.6 | - |  |  |
| 29 | `LnkObjAbsE` | Linked Doc. Internal ID | Int | 11 | - |  |  |
| 30 | `LinkObjTyp` | Linked Document Type | Int | 11 | - |  |  |
| 31 | `LinkDocNum` | Linked Document Number | Int | 11 | - |  |  |
| 32 | `LinkInsNum` | Linked Doc. Installment Number | Int | 11 | - |  |  |
| 33 | `LinkTrnsId` | Linked Doc. JE Trans. No. | Int | 11 | [OJDT](OJDT.md) |  |  |
| 34 | `LinkTrnsLn` | Linked Doc. JE Row No. | Int | 11 | - |  |  |
| 35 | `TrnsTtlAmt` | Balancing Trans. Total Amount | Num | 19.6 | - |  |  |
| 36 | `TrnsTtlFc` | Balancing Trans. Total Amt FC | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineId |
