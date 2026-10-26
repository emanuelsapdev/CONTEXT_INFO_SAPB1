# OEOY - End-of-Year Transfer

- **Tabla:** OEOY
- **Descripción:** End-of-Year Transfer
- **Cantidad de campos:** 124
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OEOY.html

## Campos (124)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `GenrlDefs` | General Definitions | VarChar | 1 | - | Y | `Y`<br>`N` |
| 2 | `ReFiles` | Transfer Template Designer Files | VarChar | 1 | - | Y | `Y`<br>`N` |
| 3 | `ActIndex` | Transfer Accounts Index | VarChar | 1 | - | Y | `Y`<br>`N` |
| 4 | `ActFromCod` | From Code | nVarChar | 15 | - |  |  |
| 5 | `ActToCode` | To Code | nVarChar | 15 | - |  |  |
| 6 | `ActGroup` | ActGroup | nVarChar | 16 | - | 255 |  |
| 7 | `CrdIndex` | Transfer Credit Card Index | VarChar | 1 | - | Y | `Y`<br>`N` |
| 8 | `CrdFromCod` | From Code | nVarChar | 15 | - |  |  |
| 9 | `CrdToCode` | To Code | nVarChar | 15 | - |  |  |
| 10 | `CrdGrpCust` | Customer Group | Int | 6 | - |  |  |
| 11 | `CrdGrpVndr` | Vendor Group | Int | 6 | - |  |  |
| 12 | `CrdToknAnd` | CrdToknAnd | VarChar | 1 | - |  |  |
| 13 | `CrdUseGrps` | CrdUseGrps | VarChar | 1 | - |  |  |
| 14 | `CrdClsRang` | CrdClsRang | VarChar | 1 | - |  |  |
| 15 | `CrdGrpData` | Properties | nVarChar | 64 | - |  |  |
| 16 | `ItmIndex` | Transfer Item Index | VarChar | 1 | - | Y | `Y`<br>`N` |
| 17 | `ItmFromCod` | From Code | nVarChar | 50 | - |  |  |
| 18 | `ItmToCode` | To Code | nVarChar | 50 | - |  |  |
| 19 | `ItmGroup` | Item Group | Int | 6 | - |  |  |
| 20 | `ItmToknAnd` | ItmToknAnd | VarChar | 1 | - |  |  |
| 21 | `ItmUseGrps` | ItmUseGrps | VarChar | 1 | - |  |  |
| 22 | `ItmClsRang` | ItmClsRang | VarChar | 1 | - |  |  |
| 23 | `ItmGrpData` | Properties | nVarChar | 64 | - |  |  |
| 24 | `TransfDoc` | Documents Transfer | VarChar | 1 | - | N | `Y`<br>`N` |
| 25 | `UnDpsChk` | Transfer Undeposited Checks | VarChar | 1 | - | N | `Y`<br>`N` |
| 26 | `DpsChk` | Transfer Postdated Checks | VarChar | 1 | - | N | `Y`<br>`N` |
| 27 | `UnDpsVouch` | Transfer Unpaid Vouchers | VarChar | 1 | - | N | `Y`<br>`N` |
| 28 | `DpsVouch` | Transfer Deffered Vouchers | VarChar | 1 | - | N | `Y`<br>`N` |
| 29 | `WorkOrder` | Open Work Instructions | VarChar | 1 | - | N | `Y`<br>`N` |
| 30 | `RcrTrt` | Posting Templates & Rec. Trans | VarChar | 1 | - | N | `Y`<br>`N` |
| 31 | `Connection` | Activities | VarChar | 1 | - | N | `Y`<br>`N` |
| 32 | `SpcPrice` | Special Prices | VarChar | 1 | - | N | `Y`<br>`N` |
| 33 | `Quotations` | Transfer Open Sales Quotations | VarChar | 1 | - | N |  |
| 34 | `Orders` | Transfer Open Orders | VarChar | 1 | - | N | `Y`<br>`N` |
| 35 | `DlvrNotes` | Transfer Open Delivery Notes | VarChar | 1 | - | N | `Y`<br>`N` |
| 36 | `DlvrInvocs` | Transfer Open Invoices | VarChar | 1 | - | N | `Y`<br>`N` |
| 37 | `P_Orders` | Transfer Purchase Orders | VarChar | 1 | - | N | `Y`<br>`N` |
| 38 | `P_Invoices` | A/P Invoices | VarChar | 1 | - | N | `Y`<br>`N` |
| 39 | `ProdTree` | Product Tree | VarChar | 1 | - | N | `Y`<br>`N` |
| 40 | `Subst` | Customer/Vendor Catalog No. | VarChar | 1 | - | N | `Y`<br>`N` |
| 41 | `Import` | Landed Costs | VarChar | 1 | - | N | `Y`<br>`N` |
| 42 | `Revert` | Returns | VarChar | 1 | - | N | `Y`<br>`N` |
| 43 | `ActBlnc` | Transfer Account Balances | VarChar | 1 | - | N | `Y`<br>`N` |
| 44 | `ActRef1` | Ref. 1 for Opening Bal. Trans. | nVarChar | 11 | - |  |  |
| 45 | `ActRef2` | Ref. 2 for Opening Bal. Trans. | nVarChar | 11 | - |  |  |
| 46 | `ActRefDate` | Posting Date for OB Transactions | Date | 8 | - |  |  |
| 47 | `ActDueDate` | Due date for OB transaction | Date | 8 | - |  |  |
| 48 | `ActMemo` | Journal Entry Details | nVarChar | 50 | - |  |  |
| 49 | `AOpnBlnAct` | Opening Balances Account | nVarChar | 15 | - |  |  |
| 50 | `AEquetyAct` | Retained Earnings Account | nVarChar | 15 | - |  |  |
| 51 | `ActExpLine` | Transfer Split Balances | VarChar | 1 | - | N | `Y` = Unreconciled Internally<br>`N`<br>`E` = Unreconciled Externally |
| 52 | `ActBlncFrC` | From Code | nVarChar | 15 | - |  |  |
| 53 | `ActBlncToC` | To Code | nVarChar | 15 | - |  |  |
| 54 | `ActBlncGrp` | ActBlncGrp | nVarChar | 16 | - | YYY |  |
| 55 | `ActZeroBln` | Account Transactions with Zero Balance | VarChar | 1 | - | Y | `Y`<br>`N` |
| 56 | `CrdBlnc` | Transfer Credit Card Balances | VarChar | 1 | - | N | `Y`<br>`N` |
| 57 | `CrdRef1` | Ref. 1 for OB Transactions | nVarChar | 11 | - |  |  |
| 58 | `CrdRef2` | Ref. 2 for OB Transactions | nVarChar | 11 | - |  |  |
| 59 | `CrdRefDate` | Posting Date for OB Transactions | Date | 8 | - |  |  |
| 60 | `CrdDueDate` | Due date for OB transaction | Date | 8 | - |  |  |
| 61 | `CrdMemo` | Journal Entry Details | nVarChar | 50 | - |  |  |
| 62 | `COpnBlnAct` | Opening Balances Account | nVarChar | 15 | - |  |  |
| 63 | `CrdExpLine` | Transfer Split Balances | VarChar | 1 | - | N | `Y`<br>`N` |
| 64 | `CrdBlncFrC` | From Code | nVarChar | 15 | - |  |  |
| 65 | `CrdBlncToC` | To Code | nVarChar | 15 | - |  |  |
| 66 | `CrdBlncGrC` | Customer Group | Int | 6 | - |  |  |
| 67 | `CrdBlnGrpV` | Vendor Group | Int | 6 | - |  |  |
| 68 | `CrdBTknAnd` | CrdBTknAnd | VarChar | 1 | - |  |  |
| 69 | `CrdBUseGrp` | CrdBUseGrp | VarChar | 1 | - |  |  |
| 70 | `CrdBClsRng` | CrdBClsRng | VarChar | 1 | - |  |  |
| 71 | `CrdBGrpDat` | Properties | nVarChar | 64 | - |  |  |
| 72 | `CrdZeroBln` | Card Transactions with Zero Balance | VarChar | 1 | - | Y | `Y`<br>`N` |
| 73 | `ItmBlnc` | Transfer Item Balances | VarChar | 1 | - | N | `Y`<br>`N` |
| 74 | `ItmRef1` | Ref. 1 for Opening Bal. Trans. | nVarChar | 11 | - |  |  |
| 75 | `ItmRef2` | Ref. 2 for Opening Bal. Trans. | nVarChar | 11 | - |  |  |
| 76 | `ItmRefDate` | Posting Date for OB Transaction | Date | 8 | - |  |  |
| 77 | `ItmMemo` | Journal Entry Details | nVarChar | 50 | - |  |  |
| 78 | `ItmBlncFrC` | From Code | nVarChar | 50 | - |  |  |
| 79 | `ItmBlncToC` | To Code | nVarChar | 50 | - |  |  |
| 80 | `ItmBlncGrp` | Item Group | Int | 6 | - |  |  |
| 81 | `ItmBTknAnd` | ItmBTknAnd | VarChar | 1 | - |  |  |
| 82 | `ItmBUseGrp` | ItmBUseGrp | VarChar | 1 | - |  |  |
| 83 | `ItmBClsRng` | ItmBClsRng | VarChar | 1 | - |  |  |
| 84 | `ItmBGrpDat` | Properties | nVarChar | 64 | - |  |  |
| 85 | `ItmPlnNum` | Transaction Price List | Int | 6 | - | 1 |  |
| 86 | `ItmZeroPr` | Transfer Items Without Price | VarChar | 1 | - | N | `Y`<br>`N` |
| 87 | `FileReport` | Create Report File | VarChar | 1 | - | Y | `Y`<br>`N` |
| 88 | `CompName` | Company Name for Transfering | nVarChar | 200 | - |  |  |
| 89 | `WasGnrlDef` | Was general data transferred | VarChar | 1 | - | N | `Y`<br>`N` |
| 90 | `P_DlvrNots` | Transfer PO Del. Notes | VarChar | 1 | - | N | `Y`<br>`N` |
| 91 | `Spg` | Transfer Discount for Groups | VarChar | 1 | - | N | `Y`<br>`N` |
| 92 | `Pdn` | Purchase Delivery Notes | VarChar | 1 | - | N | `Y`<br>`N` |
| 93 | `PdnClosed` | Closed Purchase Delivery Notes | VarChar | 1 | - | N | `Y`<br>`N` |
| 94 | `Rpd` | Revert Purchase Delivery Notes | VarChar | 1 | - | N | `Y`<br>`N` |
| 95 | `ReportTemp` | Report Templates | VarChar | 1 | - | N | `Y`<br>`N` |
| 96 | `Confirmat` | Confirmation | VarChar | 1 | - | N | `Y`<br>`N` |
| 97 | `DocDraft` | Document Drafts | VarChar | 1 | - | N | `Y`<br>`N` |
| 98 | `ChkOutDrft` | Checks for Payment Drafts | VarChar | 1 | - | N | `Y`<br>`N` |
| 99 | `OptOpen` | Open Opportunities | VarChar | 1 | - | N | `Y`<br>`N` |
| 100 | `OptClosed` | Closed Opportunities | VarChar | 1 | - | N | `Y`<br>`N` |
| 101 | `SerBtchNum` | Batch/Serial No. | VarChar | 1 | - | N | `Y`<br>`N` |
| 102 | `CorrInvoic` | Correction Invoice | VarChar | 1 | - | N | `Y`<br>`N` |
| 103 | `UserGign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 104 | `PaymDraf` | Payment Draft | VarChar | 1 | - | N | `Y`<br>`N` |
| 105 | `PaymentWiz` | Saved Payment Wizard | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 106 | `AltItems` | Alternative Items | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 107 | `DPIInvoice` | A/R Down Payment Invoice | VarChar | 1 | - | N |  |
| 108 | `DPIRequest` | A/R Down Payment Request | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 109 | `Ctr` | Service Contracts | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 110 | `Ins` | Customer Equipment Card | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 111 | `CorrAPInv` | A/P Correction Invoice | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 112 | `CorrAPRev` | A/P Correction Invoice Reversal | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 113 | `CorrARInv` | A/R Correction Invoice | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 114 | `CorrARRev` | A/R Correction Invoice Reversal | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 115 | `UserObj` | User Object | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 116 | `AdWrkOrdr` | Advanced Work Order | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 117 | `DPOInvoice` | A/P Down Payment Invoice | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 118 | `DPORequest` | A/P Down Payment Request | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 119 | `P_Quotatio` | Transfer Open Pur. Quotations | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 120 | `WTQ` | Inventory Transfer Requests | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 121 | `Oat` | Blanket Agreement | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 122 | `CPN` | Campaign | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 123 | `AdvRules` | Transfer Advanced Rules | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 124 | `Prq` | Purchase Request | VarChar | 1 | - | N |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CompName |
