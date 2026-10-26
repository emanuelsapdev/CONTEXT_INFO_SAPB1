# PEX1 - Payment Results Table - Rows

- **Tabla:** PEX1
- **Descripción:** Payment Results Table - Rows
- **Cantidad de campos:** 32
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/PEX1.html

## Campos (32)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `LineId` | Row Number | Int | 11 | - |  |  |
| 3 | `PayRunDate` | Date of Payment Run | Date | 8 | - |  |  |
| 4 | `PaymWizCod` | Payment Wizard Code | Int | 11 | - |  |  |
| 5 | `VendorNum` | Vendor Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 6 | `CustNum` | Customer Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 7 | `PaymMethod` | Payment Means | nVarChar | 15 | [OPYM](OPYM.md) |  |  |
| 8 | `PaymDocNum` | Payment Document No. | Int | 11 | - |  |  |
| 9 | `FiscalYear` | Fiscal Year | Date | 8 | - |  |  |
| 10 | `VendRefNum` | Vendor Ref. No. | nVarChar | 200 | - |  |  |
| 11 | `ObjType` | Document Object Type | nVarChar | 20 | - |  |  |
| 12 | `DocDate` | Document Posting Date | Date | 8 | - |  |  |
| 13 | `TaxDate` | Document Date | Date | 8 | - |  |  |
| 14 | `CrdGLAcct` | BP Accounts Receivable/Payable | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 15 | `DocCurr` | Document Currency | nVarChar | 3 | - |  |  |
| 16 | `DocRate` | Document Rate | Num | 19.6 | - |  |  |
| 17 | `DocTotal` | Document Total (LC) | Num | 19.6 | - |  |  |
| 18 | `DocTotalFC` | Document Total (FC) | Num | 19.6 | - |  |  |
| 19 | `DocTaxAmnt` | Tax Amount per Document Amount | Num | 19.6 | - |  |  |
| 20 | `DoxTxAmtFC` | Tax Amount per Document Amount | Num | 19.6 | - |  |  |
| 21 | `DocRemarks` | Document Remarks | nVarChar | 254 | - |  |  |
| 22 | `DocPrmTerm` | Document Payment Terms | Int | 6 | [OCTG](OCTG.md) |  |  |
| 23 | `DocPymRef` | Payment Document Reference | nVarChar | 27 | - |  |  |
| 24 | `DocLocCurr` | Document Local Currency | nVarChar | 3 | - |  |  |
| 25 | `PymTermPer` | Payment Terms Period | Int | 11 | - |  |  |
| 26 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 27 | `PymNum` | Payment Number (PWZ3 - PymNum) | Int | 11 | - |  |  |
| 28 | `PayOrderNo` | Payment Order Number | Int | 11 | [OIPO](OIPO.md) |  |  |
| 29 | `FreeText1` | Free Text 1 | nVarChar | 100 | - |  |  |
| 30 | `FreeText2` | Free Text 2 | nVarChar | 100 | - |  |  |
| 31 | `FreeText3` | Free Text 3 | nVarChar | 100 | - |  |  |
| 32 | `vatApplied` | VAT Applied | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineId |
