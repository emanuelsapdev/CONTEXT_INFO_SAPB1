# OEJB - Wizard Run Details for ERV-JAb

- **Tabla:** OEJB
- **Descripción:** Wizard Run Details for ERV-JAb
- **Cantidad de campos:** 24
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OEJB.html

## Campos (24)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `WizardId` | Wizard ID | Int | 11 | - |  |  |
| 2 | `WizardName` | Wizard Name | nVarChar | 100 | - |  |  |
| 3 | `FromDate` | From Date | Date | 8 | - |  |  |
| 4 | `ToDate` | To Date | Date | 8 | - |  |  |
| 5 | `PFromDate` | Previous Year From Date | Date | 8 | - |  |  |
| 6 | `PToDate` | Previous Year To Date | Date | 8 | - |  |  |
| 7 | `DateOfRun` | Date of Run | Date | 8 | - |  |  |
| 8 | `Status` | Status | VarChar | 1 | - | O | `O` = Open<br>`C` = Closed |
| 9 | `ActYearCl` | Classifictn in Actual Yr | VarChar | 1 | - |  | `S` = Small<br>`M` = Medium<br>`L` = Large |
| 10 | `FormFinSt` | Form of Financial Statement | Int | 11 | - | 0 | `0`<br>`1` = Small GmbH (UGB Form 2,3)<br>`2` = Small GmbH with Balance Sheet<br>`3` = Medium Large GmbH<br>`4` = AG (Eng. PLC) |
| 11 | `EBSTmpl` | E-Balance Sheet Template | Int | 11 | [OFRT](OFRT.md) |  |  |
| 12 | `EPaLTmpl` | E-P&L Template | Int | 11 | [OFRT](OFRT.md) |  |  |
| 13 | `OverwrFinS` | Overwrite Financial Statement | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 14 | `Reference` | Reference | nVarChar | 25 | - |  |  |
| 15 | `HBCode` | House Bank Code | Int | 11 | [DSC1](DSC1.md) |  |  |
| 16 | `PayRef` | Payment Reference | nVarChar | 12 | - |  |  |
| 17 | `SndrRole` | Sender Role | Int | 11 | - | 0 | `0`<br>`1` = 1 - Sole Company Representative and Signatory<br>`2` = 2 - Sole Authorized Company Representative<br>`3` = 3 - One of Authorized Company Representatives |
| 18 | `CRegNumber` | Commercial Register Number | nVarChar | 7 | - |  |  |
| 19 | `LFBSheetD` | Legal Form on Actl Bal Sht Dte | nVarChar | 3 | - |  | `AG` = Public Limited Company (AG)<br>`SC` = European Cooperative Society (SCE)<br>`SE` = Company under European Law (SE, Societa Europaea)<br>`GEN` = Industrial Cooperative Society<br>`GES` = Limited Liability Company (GmbH)<br>`KG` = Limited Partnership<br>`OG` = Open Company |
| 20 | `LFBSheetPr` | Lgl Form on Bal Sht Dte Prv Yr | nVarChar | 3 | - |  | `AG` = Public Limited Company (AG)<br>`SC` = European Cooperative Society (SCE)<br>`SE` = Company under European Law (SE, Societa Europaea)<br>`GEN` = Industrial Cooperative Society<br>`GES` = Limited Liability Company (GmbH)<br>`KG` = Limited Partnership<br>`OG` = Open Company |
| 21 | `RegNum` | Reg. No. of Partner Company | nVarChar | 7 | - |  |  |
| 22 | `CmpanyName` | Company Name | Text | 16 | - |  |  |
| 23 | `XMLFile` | XML File Storage | Text | 16 | - |  |  |
| 24 | `TimeOfRun` | Time of Run | Int | 6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | WizardId |
