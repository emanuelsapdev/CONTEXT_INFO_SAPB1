# ODWZ - Dunning Wizard

- **Tabla:** ODWZ
- **Descripción:** Dunning Wizard
- **Cantidad de campos:** 46
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ODWZ.html

## Campos (46)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WizardId` | Wizard ID | Int | 11 | - |  |  |
| 2 | `WizardName` | Wizard Name | nVarChar | 100 | - |  |  |
| 3 | `ToPayDate` | To be paid by | Date | 8 | - |  |  |
| 4 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 5 | `Status` | Wizard Status | VarChar | 1 | - | S | `S` = Saved Parameters<br>`R` = Saved Recommendations<br>`E` = Executed and Printed or Sent by E-Mail<br>`O` = Executed, Not Yet Printed or Sent by E-Mail<br>`P` = Partially Executed and Printed<br>`T` = Partially Executed, Not Yet Printed or Sent by E-Mail |
| 6 | `DunLevel` | Dunning Level | nVarChar | 3 | [ODUN](ODUN.md) | 0 | `0` = All<br>`1` = Level 1<br>`2` = Level 2<br>`3` = Level 3<br>`4` = Level 4<br>`5` = Level 5<br>`6` = Level 6<br>`7` = Level 7<br>`8` = Level 8<br>`9` = Level 9<br>`10` = Level 10 |
| 7 | `CreditZero` | Include BP with Credit | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 8 | `PayNoBased` | Payment on Account | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 9 | `CrdtNBased` | Include Credit Not Based | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 10 | `DunTime` | Dunning Time | nVarChar | 6 | - |  |  |
| 11 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 12 | `FromDate` | From Date Filter | Date | 8 | - |  |  |
| 13 | `ToDate` | Date To Filter | Date | 8 | - |  |  |
| 14 | `ManualJEs` | Include Manual JEs | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 15 | `DspOpnItms` | Display Open Items | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 16 | `AllowNegLt` | Allow Negative Dunning Letter | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 17 | `DunTerm` | Dunning Term | nVarChar | 25 | [ODUT](ODUT.md) | -1 |  |
| 18 | `FrmDueDate` | From Due Date Filter | Date | 8 | - |  |  |
| 19 | `ToDueDate` | To Due Date Filter | Date | 8 | - |  |  |
| 20 | `UpToDate` | Include Payments Up To | Date | 8 | - |  |  |
| 21 | `InvPostDat` | Invc. Posting Date | Date | 8 | - |  |  |
| 22 | `InvDueDate` | Invc. Due Date | Date | 8 | - |  |  |
| 23 | `InvDocDate` | Invc. Doc. Date | Date | 8 | - |  |  |
| 24 | `Project` | Project | nVarChar | 20 | - |  |  |
| 25 | `OcrCode` | Costing Code | nVarChar | 8 | - |  |  |
| 26 | `OcrCode2` | Costing Code 2 | nVarChar | 8 | - |  |  |
| 27 | `OcrCode3` | Costing Code 3 | nVarChar | 8 | - |  |  |
| 28 | `OcrCode4` | Costing Code 4 | nVarChar | 8 | - |  |  |
| 29 | `OcrCode5` | Costing Code 5 | nVarChar | 8 | - |  |  |
| 30 | `InVatGroup` | Interest VAT Group | nVarChar | 8 | - |  |  |
| 31 | `InTaxCode` | Interest Tax Code | nVarChar | 8 | - |  |  |
| 32 | `FeVatGroup` | Fee VAT Group | nVarChar | 8 | - |  |  |
| 33 | `FeTaxCode` | Fee Tax Code | nVarChar | 8 | - |  |  |
| 34 | `VatPrcnt` | VAT Percent | Num | 19.6 | - |  |  |
| 35 | `AutoRmk` | Auto Remark | VarChar | 1 | - | Y |  |
| 36 | `Remarks` | Remarks | nVarChar | 254 | - |  |  |
| 37 | `Series` | Series | Int | 11 | [NNM1](NNM1.md) | 0 |  |
| 38 | `BPLId` | BPL ID Assigned to Invoice | Int | 11 | - |  |  |
| 39 | `LocCode` | Location Code | Int | 11 | - |  |  |
| 40 | `VersionNum` | Version Number | nVarChar | 13 | - |  |  |
| 41 | `OvrDueOnly` | BPs with Overdue Item Only | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 42 | `QuickDisp` | Quick Display | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 43 | `OPNoBased` | Include Outgoing Payments | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 44 | `CnsdVendor` | Consider Connected Vendor | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 45 | `SACIntrst` | SAC for Interest | nVarChar | 8 | - |  |  |
| 46 | `SACFee` | SAC for Fee | nVarChar | 8 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WizardId |
| SECONDARY | No | WizardName |
