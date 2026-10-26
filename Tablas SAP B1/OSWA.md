# OSWA - Specific Withholding Amounts

- **Tabla:** OSWA
- **Descripción:** Specific Withholding Amounts
- **Cantidad de campos:** 74
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OSWA.html

## Campos (74)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `PymntRsnCd` | Payment Reason Code | nVarChar | 3 | [OPTR](OPTR.md) |  |  |
| 2 | `CardCode` | BP Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 3 | `FllTxInAdv` | Full WTax Taxation in Advance | Num | 19.6 | - |  |  |
| 4 | `AmntsOnhld` | WTax Amount on Hold | Num | 19.6 | - |  |  |
| 5 | `RTAsWth` | Regional IRPEF Held as WTax | Num | 19.6 | - |  |  |
| 6 | `RTAsAdv` | Regional IRPEF - In Advance | Num | 19.6 | - |  |  |
| 7 | `SspndRegTx` | Regional Suspended Tax - IRPEF | Num | 19.6 | - |  |  |
| 8 | `MTAsWth` | Municipal Tax as WTax - IRPEF | Num | 19.6 | - |  |  |
| 9 | `MTAsAdv` | Municipal Tax Held as Advance | Num | 19.6 | - |  |  |
| 10 | `SspndMTTx` | Suspended Municipal Tax | Num | 19.6 | - |  |  |
| 11 | `TxblPrYr` | Taxable Amt - Previous Year | Num | 19.6 | - |  |  |
| 12 | `WTHPrYr` | WTax Amount - Previous Year | Num | 19.6 | - |  |  |
| 13 | `ScrtyCntrP` | Social Security Tax Payer | Num | 19.6 | - |  |  |
| 14 | `ScrtyCntrS` | Social Security Supplier | Num | 19.6 | - |  |  |
| 15 | `ExpsRmbrsd` | Expenses Reimbursed | Num | 19.6 | - |  |  |
| 16 | `WTHRmbrsd` | WTax Reimbursed | Num | 19.6 | - |  |  |
| 17 | `DlvryIdNo` | Delivery Identification No. | nVarChar | 100 | - |  |  |
| 18 | `SnglCrtfNo` | Single Certification No. | nVarChar | 17 | - |  |  |
| 19 | `ErnYr` | Earning Year | Int | 6 | - |  |  |
| 20 | `Advanced` | Advanced | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 21 | `WTHTypCd` | WTax Type Code | nVarChar | 2 | [OWXT](OWXT.md) |  |  |
| 22 | `GrssAmount` | Gross Amount Due to Supplier | Num | 19.6 | - |  |  |
| 23 | `NtSbjctFrg` | Amount Not Subject to WT | Num | 19.6 | - |  |  |
| 24 | `TxblAmnt` | Taxable Amount | Num | 19.6 | - |  |  |
| 25 | `WTHAmnt` | Withholding Tax Amount | Num | 19.6 | - |  |  |
| 26 | `SSFiscalCd` | Social Security Fiscal C..(29) | nVarChar | 16 | - |  |  |
| 27 | `SSIName` | Social Security Institut..(30) | nVarChar | 100 | - |  |  |
| 28 | `SSICode` | Social Security Institut..(31) | VarChar | 1 | - |  | `2` = ENPAM<br>`4` = ENPAPI |
| 29 | `CompanyCd` | Company Code(32) | nVarChar | 16 | - |  |  |
| 30 | `Category` | Category(33) | nVarChar | 3 | [OWCT](OWCT.md) |  |  |
| 31 | `EmpeSSCntr` | Employee social security..(34) | Num | 19.6 | - |  |  |
| 32 | `EmprSSCntr` | Employer social security..(35) | Num | 19.6 | - |  |  |
| 33 | `OthCntrbts` | Other Contributions(36) | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 34 | `VOthCntrbt` | Value of Other Contribut..(37) | Num | 19.6 | - |  |  |
| 35 | `OthAmntDue` | Other amounts due(38) | Num | 19.6 | - |  |  |
| 36 | `OthAmntPd` | Other amounts paid(39) | Num | 19.6 | - |  |  |
| 37 | `AmntPdBfBr` | Amount Paid before Bankr..(41) | Num | 19.6 | - |  |  |
| 38 | `AmntPdByTr` | Amount Paid by Trustee(42) | Num | 19.6 | - |  |  |
| 39 | `FiscalCode` | Fiscal Code(52) | nVarChar | 16 | - |  |  |
| 40 | `TxblAmntE` | Taxable Amount(53) | Num | 19.6 | - |  |  |
| 41 | `TaxAmount` | Tax Amount(54) | Num | 19.6 | - |  |  |
| 42 | `TxAmntInAd` | Tax Amount in Advance(55) | Num | 19.6 | - |  |  |
| 43 | `SspndWTHTx` | Suspended WTH Tax(56) | Num | 19.6 | - |  |  |
| 44 | `AdRgTxIRPH` | Additional Regional tax..(57) | Num | 19.6 | - |  |  |
| 45 | `AdRgTxIRPA` | Additional Regional tax..(58) | Num | 19.6 | - |  |  |
| 46 | `SspdRgnlTx` | Suspended Regional Tax(59) | Num | 19.6 | - |  |  |
| 47 | `AdCtTxIRWT` | Additional City tax to I..(60) | Num | 19.6 | - |  |  |
| 48 | `AdCtTxIWTA` | Additional City Tax to I..(61) | Num | 19.6 | - |  |  |
| 49 | `SspndCtTx` | Suspended City Tax(62) | Num | 19.6 | - |  |  |
| 50 | `FsCdTrdPty` | Fiscal Code Third Party(71) | nVarChar | 16 | - |  |  |
| 51 | `FCdTrdPtyS` | Fiscal Code Third Party..(72) | nVarChar | 16 | - |  |  |
| 52 | `FscCdExpr` | Fiscal Code Expropriation(73) | nVarChar | 16 | - |  |  |
| 53 | `FsCdMnDbS` | Fiscal Code of Main Deb..(101) | nVarChar | 16 | - |  |  |
| 54 | `AmntPdS` | Amount Paid(102) | Num | 19.6 | - |  |  |
| 55 | `WHTApdS` | WHT Applied(103) | Num | 19.6 | - |  |  |
| 56 | `WHTNApdS` | WHT not Applied(104) | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 57 | `FsCdMnDbR` | Fiscal Code of Main Deb..(105) | nVarChar | 16 | - |  |  |
| 58 | `AmntPdR` | Amount Paid(106) | Num | 19.6 | - |  |  |
| 59 | `WHTApdR` | WHT Applied(107) | Num | 19.6 | - |  |  |
| 60 | `WHTNApdR` | WHT not Applied(108) | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 61 | `AmntPdA` | Amount Paid(131) | Num | 19.6 | - |  |  |
| 62 | `TxAppldA` | Tax Applied(132) | Num | 19.6 | - |  |  |
| 63 | `AmntPdB` | Amount Paid(133) | Num | 19.6 | - |  |  |
| 64 | `TxAppldB` | Tax Applied(134) | Num | 19.6 | - |  |  |
| 65 | `AmntPdC` | Amount Paid(135) | Num | 19.6 | - |  |  |
| 66 | `TxAppldC` | Tax Applied(136) | Num | 19.6 | - |  |  |
| 67 | `AmntPdD` | Amount Paid(137) | Num | 19.6 | - |  |  |
| 68 | `TxAppldD` | Tax Applied(138) | Num | 19.6 | - |  |  |
| 69 | `AmtPvdNTxS` | Amounts provided and no..(104) | Num | 19.6 | - |  |  |
| 70 | `AmtPvdNTxR` | Amounts provided and no..(108) | Num | 19.6 | - |  |  |
| 71 | `CUSplit` | CU Split | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 72 | `SmRnNtWTx` | Returned Amount After Deduction of WTax | Num | 19.6 | - |  |  |
| 73 | `WHTRelCode` | Relation Type (31) | nVarChar | 3 | [OWRT](OWRT.md) |  |  |
| 74 | `AmtDedUsed` | Deductible amount used (40) | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | PymntRsnCd, CardCode, CUSplit |
