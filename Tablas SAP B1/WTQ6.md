# WTQ6 - Inventory Transfer Request - Installments

- **Tabla:** WTQ6
- **Descripción:** Inventory Transfer Request - Installments
- **Cantidad de campos:** 65
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/WTQ6.html

## Campos (65)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Internal Document ID | Int | 11 | [OWTQ](OWTQ.md) |  |  |
| 2 | `InstlmntID` | Installment ID | Int | 6 | - | 1 |  |
| 3 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 1250000001 |  |
| 4 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 5 | `DueDate` | Due Date | Date | 8 | - |  |  |
| 6 | `Status` | Installment Status | VarChar | 1 | - | O | `O` = Open<br>`C` = Closed |
| 7 | `DunnLevel` | Dunning Level | Int | 11 | - | 0 |  |
| 8 | `InsTotal` | Total Installment | Num | 19.6 | - |  |  |
| 9 | `InsTotalFC` | Total Installment (FC) | Num | 19.6 | - |  |  |
| 10 | `InsTotalSy` | Total Installment (SC) | Num | 19.6 | - |  |  |
| 11 | `PaidToDate` | Paid to Date | Num | 19.6 | - |  |  |
| 12 | `PaidFC` | Paid (FC) | Num | 19.6 | - |  |  |
| 13 | `PaidSys` | Paid (SC) | Num | 19.6 | - |  |  |
| 14 | `VatSum` | Total Tax | Num | 19.6 | - |  |  |
| 15 | `VatSumFC` | Tax Amount (FC) | Num | 19.6 | - |  |  |
| 16 | `VatSumSy` | Tax Amount (SC) | Num | 19.6 | - |  |  |
| 17 | `VatPaid` | Tax Paid to Date | Num | 19.6 | - |  |  |
| 18 | `VatPaidFC` | Tax Paid (FC) | Num | 19.6 | - |  |  |
| 19 | `VatPaidSys` | Tax Paid (SC) | Num | 19.6 | - |  |  |
| 20 | `TotalExpns` | Total Freight Charges | Num | 19.6 | - |  |  |
| 21 | `TotalExpFC` | Total Freight Charges (FC) | Num | 19.6 | - |  |  |
| 22 | `TotalExpSC` | Total Freight Charges (SC) | Num | 19.6 | - |  |  |
| 23 | `ExpAppl` | Applied Freight Charges | Num | 19.6 | - |  |  |
| 24 | `ExpApplFC` | Applied Freight Charges (FC) | Num | 19.6 | - |  |  |
| 25 | `ExpApplSC` | Applied Freight Charges (SC) | Num | 19.6 | - |  |  |
| 26 | `WTSum` | WTax Amount | Num | 19.6 | - |  |  |
| 27 | `WTSumFC` | WTax Amount (FC) | Num | 19.6 | - |  |  |
| 28 | `WTSumSC` | WTax Amount (SC) | Num | 19.6 | - |  |  |
| 29 | `WTApplied` | Applied WTax | Num | 19.6 | - |  |  |
| 30 | `WTAppliedF` | Applied WTax (FC) | Num | 19.6 | - |  |  |
| 31 | `WTAppliedS` | Applied WTax (SC) | Num | 19.6 | - |  |  |
| 32 | `TotalBlck` | Total Reserved Amount | Num | 19.6 | - |  |  |
| 33 | `TotalBlckF` | Total Reserved Amount (FC) | Num | 19.6 | - |  |  |
| 34 | `TotalBlckS` | Total Reserved Amount (SC) | Num | 19.6 | - |  |  |
| 35 | `VATBlck` | Reserved Tax Amount | Num | 19.6 | - |  |  |
| 36 | `VATBlckFC` | Reserved Tax Amount (FC) | Num | 19.6 | - |  |  |
| 37 | `VATBlckSC` | Reserved Tax Amount (SC) | Num | 19.6 | - |  |  |
| 38 | `ExpnsBlck` | Reserved Freight Charges | Num | 19.6 | - |  |  |
| 39 | `ExpnsBlckF` | Reserved Freight Charges (FC) | Num | 19.6 | - |  |  |
| 40 | `ExpnsBlckS` | Reserved Freight Charges (SC) | Num | 19.6 | - |  |  |
| 41 | `WTBlocked` | Reserved WTax Amount | Num | 19.6 | - |  |  |
| 42 | `WTBlockedF` | Reserved WTax Amount (FC) | Num | 19.6 | - |  |  |
| 43 | `WTBlockedS` | Reserved WTax Amount (SC) | Num | 19.6 | - |  |  |
| 44 | `InstPrcnt` | Installment % | Num | 19.6 | - |  |  |
| 45 | `DunWizBlck` | Wizard Dunning Block | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 46 | `DunDate` | Last Dunning Date | Date | 8 | - |  |  |
| 47 | `Paid` | Paid | Num | 19.6 | - |  |  |
| 48 | `PaidFrgn` | Paid (FC) | Num | 19.6 | - |  |  |
| 49 | `PaidSc` | Paid (SC) | Num | 19.6 | - |  |  |
| 50 | `reserved` | Reserved | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 51 | `TaxOnExp` | Tax on Freight | Num | 19.6 | - |  |  |
| 52 | `TaxOnExpFc` | Tax on Expenses (FC) | Num | 19.6 | - |  |  |
| 53 | `TaxOnExpSc` | Tax on Expenses (SC) | Num | 19.6 | - |  |  |
| 54 | `TaxOnExpAp` | Applied Tax on Expenses | Num | 19.6 | - |  |  |
| 55 | `TaxOnExApF` | Applied Tax on Expenses (FC) | Num | 19.6 | - |  |  |
| 56 | `TaxOnExApS` | Applied Tax on Expenses (SC) | Num | 19.6 | - |  |  |
| 57 | `TaxOnExBlo` | Reserved Tax on Freight Amount | Num | 19.6 | - |  |  |
| 58 | `TaxOnExBlF` | Reserved Tax on Freight Amt FC | Num | 19.6 | - |  |  |
| 59 | `TaxOnExBlS` | Reserved Tax on Freight Amt SC | Num | 19.6 | - |  |  |
| 60 | `LvlUpdDate` | Dunning Level Update Date | Date | 8 | - |  |  |
| 61 | `Ordered` | Payment Ordered | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 62 | `PaidDpm` | Paid by Down Payment | Num | 19.6 | - |  |  |
| 63 | `PaidDpmFc` | Paid by Down Payment (FC) | Num | 19.6 | - |  |  |
| 64 | `PaidDpmSc` | Paid by Down Payment (SC) | Num | 19.6 | - |  |  |
| 65 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, InstlmntID |
