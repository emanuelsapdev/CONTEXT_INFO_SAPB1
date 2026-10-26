# VRW2 - VAT Reposting Wizard - Rows 2

- **Tabla:** VRW2
- **Descripción:** VAT Reposting Wizard - Rows 2
- **Cantidad de campos:** 35
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/VRW2.html

## Campos (35)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `TaxInvID` | A/P Tax Invoice ID | Int | 11 | [OTPI](OTPI.md) |  |  |
| 3 | `VatGroup` | VAT Group Code | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 4 | `Selected` | Selected Line | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 5 | `LineStatus` | Line Status | VarChar | 1 | - | R | `C` = Canceled<br>`R` = Regular |
| 6 | `DebitAcc` | Debit Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 7 | `DocDate` | Document Date | Date | 8 | - |  |  |
| 8 | `VatAmount` | VAT Amount | Num | 19.6 | - |  |  |
| 9 | `NetAmount` | Net Amount | Num | 19.6 | - |  |  |
| 10 | `JETransID` | Journal Entry Number | Int | 11 | [OJDT](OJDT.md) |  |  |
| 11 | `Ref1` | Reference 1 | nVarChar | 200 | - |  |  |
| 12 | `Ref2` | Reference 2 | nVarChar | 200 | - |  |  |
| 13 | `Ref3` | Reference 3 | nVarChar | 200 | - |  |  |
| 14 | `Remarks` | Journal Entry Remarks | nVarChar | 254 | - |  |  |
| 15 | `TrnsCode` | Code | nVarChar | 4 | - |  |  |
| 16 | `BPLId` | Branch | Int | 11 | [OBPL](OBPL.md) |  |  |
| 17 | `ARINVAbs` | First A/R Invoice Abs Entry | Int | 11 | - | 0 |  |
| 18 | `ARDocNumAb` | A/R Document No. | nVarChar | 20 | - |  |  |
| 19 | `ARAbsEntry` | A/R Document Abs Entry | Int | 11 | - | 0 |  |
| 20 | `ARObjType` | A/R Document Object Type | nVarChar | 20 | - |  |  |
| 21 | `ARDocDate` | A/R Document Date | Date | 8 | - |  |  |
| 22 | `CstmrCode` | Customer Code | nVarChar | 15 | - |  |  |
| 23 | `CstmrName` | Customer Name | nVarChar | 200 | - |  |  |
| 24 | `TpiDocNum` | A/P Tax Invoice No. | Int | 11 | - |  |  |
| 25 | `TpiDocDate` | A/P Tax Invoice Posting Date | Date | 8 | - |  |  |
| 26 | `VendorCode` | Vendor Code | nVarChar | 15 | - |  |  |
| 27 | `VendorName` | Vendor Name | nVarChar | 200 | - |  |  |
| 28 | `ARDocMemo` | A/R Document Remarks | nVarChar | 254 | - |  |  |
| 29 | `TpiMemo` | A/P Tax Invoice Remarks | nVarChar | 254 | - |  |  |
| 30 | `GrsAmt` | Gross Amount | Num | 19.6 | - |  |  |
| 31 | `VatAcc` | VAT Account | nVarChar | 15 | - |  |  |
| 32 | `OpenVatAmt` | Open VAT Amount | Num | 19.6 | - |  |  |
| 33 | `OpenNetAmt` | Open Net Amount | Num | 19.6 | - |  |  |
| 34 | `OpenGrsAmt` | Open Gross Amount | Num | 19.6 | - |  |  |
| 35 | `RepstedVat` | Reposted VAT | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, TaxInvID, VatGroup, ARINVAbs |
