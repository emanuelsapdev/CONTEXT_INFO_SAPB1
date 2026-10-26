# AEC8 - Electronic Document Import Files - History

- **Tabla:** AEC8
- **Descripción:** Electronic Document Import Files - History
- **Cantidad de campos:** 25
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AEC8.html

## Campos (25)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal ID | Int | 11 | - |  |  |
| 2 | `Code` | Code | Int | 11 | - |  | `0` = Invalid<br>`1` = GEN<br>`2` = EET<br>`3` = CFDI<br>`4` = FPA<br>`5` = MTD<br>`6` = EWB<br>`7` = PEPPOL<br>`8` = HOI<br>`9` = MYF<br>`10` = EIS<br>`11` = IIS<br>`12` = IIS_ANNUAL<br>`13` = DIGIPOORT<br>`14` = E-Books<br>`15` = DOX<br>`16` = RTIE<br>`17` = E-Billing<br>`18` = Tax Service<br>`19` = AFE<br>`20` = Document Signature<br>`21` = KSeF<br>`22` = GSTReturn<br>`23` = PT Document Signature<br>`24` = Skat DK<br>`25` = EII<br>`26` = NFe<br>`27` = PT eInvoicing<br>`28` = PT Electronic Communications<br>`29` = Veri*factu<br>`30` = BAS<br>`31` = PDF with XML Attachment<br>`32` = FReINV<br>`33` = euBP<br>`34` = ILOI<br>`35` = EDGT<br>`36` = EDCR<br>`37` = NAV |
| 3 | `ParentID` | Parent ID | Int | 11 | - |  |  |
| 4 | `ActType` | Action Type | Int | 11 | - | 0 | `1` = Setup<br>`2` = Report<br>`3` = A/R Document<br>`4` = A/P Document<br>`5` = A/R Draft Document<br>`6` = A/P Draft Document<br>`7` = Other<br>`8` = Skip<br>`9` = Contingency<br>`10` = BP Check<br>`11` = Incoming Payment<br>`12` = Outgoing Payment<br>`13` = Internal Reconciliation<br>`14` = Transportation Document<br>`15` = Inventory Transfer<br>`16` = VAT Obligations<br>`17` = VAT Declarations<br>`18` = VAT Liabilities<br>`19` = VAT Payments<br>`20` = Delivery<br>`21` = Return<br>`22` = A/R Invoice<br>`23` = A/R Credit Memo<br>`24` = Goods Receipt PO<br>`25` = Goods Return<br>`26` = A/P Invoice<br>`27` = A/P Credit Memo<br>`28` = Draft Incoming Payment<br>`29` = Draft Outgoing Payment<br>`30` = Journal Entry<br>`31` = E-Books Expense<br>`45` = Goods Issue<br>`46` = Goods Receipt<br>`47` = Pick List<br>`48` = Draft Goods Issue<br>`49` = Draft Goods Receipt |
| 5 | `ActDesc` | Action Description | nVarChar | 100 | - |  |  |
| 6 | `ActStatus` | Action Status | VarChar | 1 | - | N | `N` = New<br>`P` = Pending<br>`E` = Error<br>`T` = Temporary Error<br>`O` = OK<br>`S` = Sent<br>`R` = Document Error<br>`W` = Waiting<br>`A` = Authorized<br>`I` = In Process<br>`J` = Rejected<br>`D` = Denied<br>`C` = Canceled<br>`B` = Aborted<br>`Q` = Queued<br>`M` = Imported<br>`G` = Warning<br>`V` = Approved<br>`F` = Approving<br>`H` = Rejecting<br>`K` = Generated<br>`Y` = Ready to Process<br>`L` = Determined<br>`m` = Disputing<br>`y` = Dispute |
| 7 | `ActMessage` | Action Message | nVarChar | 254 | - |  |  |
| 8 | `TestMode` | Test Mode | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 9 | `GUID` | GUID | nVarChar | 100 | - |  |  |
| 10 | `Authority` | Authorities Code | nVarChar | 16 | - |  |  |
| 11 | `ProcSource` | Processing Source | nVarChar | 20 | - |  |  |
| 12 | `MetaData` | Metadata | Text | 16 | - |  |  |
| 13 | `MIMEType` | MIME Type | nVarChar | 128 | - |  |  |
| 14 | `FileName` | File Name | Text | 16 | - |  |  |
| 15 | `CardCode` | BP Code | nVarChar | 15 | - |  |  |
| 16 | `DocDate` | Document Date | Date | 8 | - |  |  |
| 17 | `ObjType` | Object Type | nVarChar | 20 | - |  |  |
| 18 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 19 | `CreateTS` | Creation Time - Incl. Secs. | Int | 11 | - |  |  |
| 20 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 21 | `UpdateTS` | Update Time - Incl. Secs. | Int | 11 | - |  |  |
| 22 | `UserSign` | User Signature | Int | 6 | - |  |  |
| 23 | `UserSign2` | Updating User | Int | 6 | - |  |  |
| 24 | `AssignedID` | Assigned ID | nVarChar | 100 | - |  |  |
| 25 | `IsBPManual` | BP is Set Manually | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| ACTION | Yes | Code, AbsEntry |
