# OLLF - Legal List Format

- **Tabla:** OLLF
- **Descripción:** Legal List Format
- **Cantidad de campos:** 16
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OLLF.html

## Campos (16)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - |  |  |
| 2 | `Name` | Electronic File Name | nVarChar | 100 | - |  |  |
| 3 | `Descr` | Electronic File Description | nVarChar | 250 | - |  |  |
| 4 | `MenuGuid` | GUID of Menu Entry | nVarChar | 32 | - |  |  |
| 5 | `Version` | Electronic File Version | nVarChar | 5 | - |  |  |
| 6 | `SchVersion` | Electronic File Schema Version | nVarChar | 5 | - |  |  |
| 7 | `OutPath` | Output Path | Text | 16 | - |  |  |
| 8 | `FrmId` | OFRM Internal ID | Int | 11 | [OFRM](OFRM.md) |  |  |
| 9 | `UpdateNum` | Update Count | Int | 11 | - | 0 |  |
| 10 | `MenuName` | Menu Name | nVarChar | 100 | - |  |  |
| 11 | `MenuPath` | Menu Path | nVarChar | 250 | - |  |  |
| 12 | `Assigned` | Format Status | nVarChar | 10 | - | N | `A` = Assigned<br>`N` = Not Assigned<br>`D` = Deleted |
| 13 | `SboVersion` | Compatible Release Version | nVarChar | 13 | - |  |  |
| 14 | `Type` | Format Type | nVarChar | 5 | - | L | `AR` = Electronic Document<br>`L` = Generic Electronic File<br>`LI` = Generic Electronic File for Intrastat<br>`ARA` = Electronic Authority Report<br>`INTER` = Internally Used<br>`IM` = Electronic Document - Input Message<br>`GD` = General Electronic Document<br>`GWS` = General Mapping for Web Service<br>`GI` = General Mapping for Document Import<br>`NFeD` = NF-e Invoice Document<br>`NFeC` = NF-e Cancelation Document<br>`NFeS` = NF-e Number Skipping Request<br>`NFeWS` = Web Service Mapping<br>`CFDD` = CFDi Electronic Document<br>`CFDP` = CFDi Electronic Payment & Reconciliation Document<br>`CFDT` = CFDI Electronic Transfer Document<br>`CFDIM` = CFDI Electronic Input Message Document<br>`CFDWS` = CFDi Electronic Mapping for Web Service<br>`EETD` = EET Electronic Document<br>`EETWS` = EET Electronic Mapping for Web Service<br>`FPAD` = FatturaPA Electronic Document<br>`FPAPD` = "FatturaPA" Electronic Purchasing Document<br>`FPAI` = FatturaPA Electronic Document for Import<br>`FPAWS` = FatturaPA Electronic Mapping for Web Service<br>`MTDR` = Making Tax Digital Report Submission<br>`MTDWS` = Making Tax Digital Mapping for Web Service<br>`EISD` = Electronic Document<br>`EISWS` = Electronic Document Web Service<br>`IISD1` = Electronic Document for IIS INV<br>`IISD2` = Electronic Document for IIS PCH<br>`IISD3` = Electronic Document for IIS Deferred<br>`IISD4` = Electronic Document for IIS JE<br>`IISD5` = Electronic Document for IIS JE Received<br>`IISWS` = Electronic Document for IIS Web Service<br>`ANND1` = Electronic Document for IIS Annual<br>`ANND2` = Electronic Document for IIS Annual Cancel<br>`ANNWS` = Electronic Document for IIS Annual Web Service<br>`PPLD` = Electronic Document for PEPPOL Invoice<br>`PPLWS` = Electronic Document for PEPPOL Web Service<br>`PPLCM` = Electronic Document for PEPPOL Credit Note<br>`PPLI` = Electronic Document for PEPPOL Import<br>`EBKD` = Electronic Document for E-Books<br>`EBKI` = Electronic Document for E-Books Income Classification<br>`EBKE` = Electronic Document for E-Books Expense Classification<br>`EBKR` = Electronic Document for E-Books Request Documents<br>`EBKRS` = Electronic Document for E-Books Request Submitted Documents<br>`EBKC` = Electronic Document for Cancellation<br>`EBKW` = Electronic Document for E-Books Web Service<br>`DOXD` = Electronic Document for Document Information Extraction<br>`DOXI` = Electronic Document for Document Information Extraction Import<br>`EWBD` = Electronic Document for E-Way Bill<br>`EINVD` = Electronic Document for E-Billing<br>`RTIED` = Electronic Document for RTIE<br>`RCTED` = Electronic Correction Document for RTIE<br>`RTIWS` = Electronic Document for RTIE Web Service<br>`AFED` = Electronic Documents for Argentina<br>`TROD` = Electronic Transportation Documents for Argentina<br>`AFEWS` = Electronic Documents for Argentina Web Service<br>`KSeF` = KSeF Document for Poland<br>`GST58` = GST Returns for BAS Report F5 F8<br>`GST7` = GST Returns for BAS Report F7<br>`SAFT` = Report SAF-T for Portugal<br>`SkatR` = Electronic Document for RSU Gateway Report Submission<br>`ILED` = Electronic Document for Israel<br>`PTSig` = Portugal E-docs Signing Process<br>`FEAP` = Portugal Electronic Invoicing in Public Administration<br>`VFact` = Veri*factu Document for Spain<br>`XMLD` = Electronic Document PDF with XML Attachment<br>`CAEAR` = Electronic Document for Argentina CAEA Request<br>`FReIN` = Electronic Invoice in France<br>`FReIM` = Electronic Invoice in France<br>`FReTR` = Electronic Report for France B2B and B2C Transaction Data<br>`FRePR` = Electronic Report for France B2B and B2C Payment Data<br>`euBP` = Electronic Tax Audit Document for Germany<br>`ILOI` = Open Interface Report for Israel<br>`NAV` = Electronic Document for Hungary |
| 15 | `SubType` | Format Subtype | nVarChar | 6 | - |  | None<br>`I` = Intrastat<br>`N` = Normal Generic File Format |
| 16 | `FileName` | File Name | Text | 16 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| NAME | Yes | Name |
