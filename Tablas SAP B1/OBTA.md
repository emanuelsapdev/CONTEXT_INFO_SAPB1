# OBTA - Brazil - Tax Adjustment

- **Tabla:** OBTA
- **Descripción:** Brazil - Tax Adjustment
- **Cantidad de campos:** 48
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBTA.html

## Campos (48)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal ID | Int | 11 | - |  |  |
| 2 | `Status` | Status | VarChar | 1 | - | O | `O` = Open<br>`C` = Canceled |
| 3 | `Canceled` | Canceled | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 4 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 5 | `DocRate` | Document Rate | Num | 19.6 | - |  |  |
| 6 | `TaxCat` | Tax Category | Int | 11 | - |  |  |
| 7 | `Type` | Type | Int | 6 | - | 1 | `1` = Referred Collection Document<br>`2` = Other Obligations, Adjustments, and Information Originating from Fiscal Documents<br>`3` = Adjustment of ICMS Appraisal<br>`4` = Adjustment and Additional Information of ICMS Appraisal<br>`5` = Adjustment of ICMS and Identification of Fiscal Documents<br>`6` = ICMS Obligations to Pay or Paid - Own Operations<br>`7` = Adjustment of ICMS-ST Appraisal<br>`8` = Adjustment and Additional Information of ICMS-ST Appraisal<br>`9` = Adjustment of ICMS-ST and Identification of Fiscal Documents<br>`10` = ICMS-ST Obligations to Pay or Paid - Own Operations<br>`11` = Adjustment of IPI Appraisal<br>`12` = Adjustment of PIS Appraisal<br>`13` = Adjustment of COFINS appraisal |
| 8 | `Oper` | Operation | Int | 6 | - | 1 | `1` = Other Debits<br>`2` = Chargeback of Debits<br>`3` = Other Credits<br>`4` = Credit Chargeback<br>`5` = Tax Deductions Calculated |
| 9 | `RefVisType` | Referenced Document ID | Int | 11 | - | 1 | `1` = A/R Invoices<br>`2` = A/P Invoices<br>`3` = A/R Credit Memos<br>`4` = A/P Credit Memos<br>`5` = Deliveries<br>`6` = Goods Receipt PO<br>`7` = A/R Reserve Invoices<br>`8` = A/P Reserve Invoices<br>`9` = External Document |
| 10 | `RefObjType` | Referenced Document Type | Int | 11 | - |  | `13` = A/R Invoices<br>`18` = A/P Invoices<br>`14` = A/R Credit Memos<br>`19` = A/P Credit Memos<br>`15` = Deliveries<br>`20` = Goods Receipt PO<br>`-1` = External Document |
| 11 | `RefDocEnt` | Referenced Document Entry | Int | 11 | - |  |  |
| 12 | `RefDocNum` | Referenced Document Number | Int | 11 | - |  |  |
| 13 | `StateUf` | State - UF | nVarChar | 2 | - |  |  |
| 14 | `PostDate` | Posting Date | Date | 8 | - |  |  |
| 15 | `CodDa` | Collection Document | VarChar | 1 | - | 1 | `1` = GNRE<br>`2` = Other Document |
| 16 | `NumDa` | Document Number | nVarChar | 20 | - |  |  |
| 17 | `CodAut` | Bank Authentication | nVarChar | 30 | - |  |  |
| 18 | `VlDa` | Total Value | Num | 19.6 | - |  |  |
| 19 | `VlDaSc` | Total Value SC | Num | 19.6 | - |  |  |
| 20 | `DtVcto` | Due Date | Date | 8 | - |  |  |
| 21 | `DtPgto` | Payment Date | Date | 8 | - |  |  |
| 22 | `CodAj` | ICMS Code | nVarChar | 10 | - |  |  |
| 23 | `DescCompAj` | Remarks | nVarChar | 120 | - |  |  |
| 24 | `BcIcms` | ICMS Base Amount | Num | 19.6 | - |  |  |
| 25 | `BcIcmsSc` | ICMS Base Amount SC | Num | 19.6 | - |  |  |
| 26 | `AliqIcms` | ICMS Rate | Num | 19.6 | - |  |  |
| 27 | `VlIcms` | ICMS Value | Num | 19.6 | - |  |  |
| 28 | `VlIcmsSc` | ICMS Value SC | Num | 19.6 | - |  |  |
| 29 | `VlOutros` | Other Values | Num | 19.6 | - |  |  |
| 30 | `CodAjApur` | Adjustment Code | nVarChar | 10 | - |  |  |
| 31 | `NumProc` | Procedure Docket Number | nVarChar | 10 | - |  |  |
| 32 | `IndProc` | Procedure Docket Indicator | VarChar | 1 | - |  |  |
| 33 | `Ser` | Fiscal Document Serial | nVarChar | 3 | - |  |  |
| 34 | `Sub` | Fiscal Document Subserial | nVarChar | 3 | - |  |  |
| 35 | `NumDoc` | Fiscal Document Number | Int | 11 | - |  |  |
| 36 | `DtDoc` | Fiscal Document Issue Date | Date | 8 | - |  |  |
| 37 | `CodMod` | Model Document Number | nVarChar | 6 | - |  |  |
| 38 | `CodPart` | BP Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 39 | `CodRec` | Revenue Code | nVarChar | 15 | - |  |  |
| 40 | `GLAcct` | G/L Account Code | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 41 | `ItemCode` | Item Code | nVarChar | 50 | [OITM](OITM.md) |  |  |
| 42 | `BPLId` | Branch ID | Int | 11 | [OBPL](OBPL.md) |  |  |
| 43 | `UserSign` | User Signature | Int | 6 | - |  |  |
| 44 | `UserSign2` | Updating User | Int | 6 | - |  |  |
| 45 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 46 | `CreateTime` | Generation Time | Int | 6 | - |  |  |
| 47 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 48 | `TransId` | Transaction Number | Int | 11 | [OJDT](OJDT.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| NUM | Yes | DocNum |
