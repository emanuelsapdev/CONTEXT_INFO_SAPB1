# ITR1 - Internal Reconciliation - Rows

- **Tabla:** ITR1
- **Descripción:** Internal Reconciliation - Rows
- **Cantidad de campos:** 26
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ITR1.html

## Campos (26)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ReconNum` | Reconciliation Number | Int | 11 | [OITR](OITR.md) |  |  |
| 2 | `LineSeq` | Row Number | Int | 11 | - |  |  |
| 3 | `ShortName` | BP/Account Code | nVarChar | 15 | - |  |  |
| 4 | `TransId` | Transaction Internal ID | Int | 11 | [OJDT](OJDT.md) |  |  |
| 5 | `TransRowId` | Transaction Row Number | Int | 11 | - |  |  |
| 6 | `SrcObjTyp` | Source Object Type | nVarChar | 20 | - |  | `30` = Journal Transactions<br>`13` = Invoices<br>`18` = Purchases<br>`24` = Receipts<br>`46` = Outgoing Payments<br>`14` = Revert Invoices<br>`19` = Revert Purchases<br>`203` = Down Payment Incoming<br>`204` = Down Payment Outgoing<br>`163` = Correction A/P Invoice<br>`164` = Correction A/P Invoice Reversals<br>`165` = Correction A/R Invoice<br>`166` = Correction A/R Invoice Reversals |
| 7 | `SrcObjAbs` | Source Object Internal ID | Int | 11 | - |  |  |
| 8 | `ReconSum` | Reconciliation Amount | Num | 19.6 | - |  |  |
| 9 | `ReconSumFC` | Reconciliation Amount (FC) | Num | 19.6 | - |  |  |
| 10 | `ReconSumSC` | Reconciliation Amount (SC) | Num | 19.6 | - |  |  |
| 11 | `FrgnCurr` | Foreign Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 12 | `SumMthCurr` | Amt in Reconciliation Currency | Num | 19.6 | - |  |  |
| 13 | `IsCredit` | Credit or Debit | VarChar | 1 | - |  | `C` = Credit<br>`D` = Debit |
| 14 | `Account` | Account Code | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 15 | `CashDisSum` | Cash Discount Amount | Num | 19.6 | - |  |  |
| 16 | `WTSum` | Withholding Tax Amount | Num | 19.6 | - |  |  |
| 17 | `WTSumFC` | Withholding Tax Amount (FC) | Num | 19.6 | - |  |  |
| 18 | `WTSumSC` | Withholding Tax Amount (SC) | Num | 19.6 | - |  |  |
| 19 | `ExpSum` | Freight Amount | Num | 19.6 | - |  |  |
| 20 | `ExpSumFC` | Freight Amount (FC) | Num | 19.6 | - |  |  |
| 21 | `ExpSumSC` | Freight Amount (SC) | Num | 19.6 | - |  |  |
| 22 | `netBefDisc` | Net Before Discount Sum | Num | 19.6 | - |  |  |
| 23 | `MIEntry` | MI Entry Include this Recon. | Int | 11 | - | 0 |  |
| 24 | `MIType` | MI Type Include this Recon. | nVarChar | 20 | - |  | `270` = A/R Monthly Invoice<br>`140000014` = A/P Monthly Invoice |
| 25 | `InstID` | Installment ID | Int | 11 | - | 0 |  |
| 26 | `IntrsStat` | Interest Letter Status | VarChar | 1 | - | U | `U` = Not Sent<br>`S` = Sent<br>`C` = Closed |

## Claves e índices (3)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ReconNum, LineSeq |
| Journal | No | TransId, TransRowId |
| Object | No | SrcObjTyp, SrcObjAbs |
