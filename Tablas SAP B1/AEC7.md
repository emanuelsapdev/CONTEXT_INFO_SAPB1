# AEC7 - Export Mapping Determination

- **Tabla:** AEC7
- **Descripción:** Export Mapping Determination
- **Cantidad de campos:** 17
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AEC7.html

## Campos (17)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal ID | Int | 11 | - |  |  |
| 2 | `Code` | Protocol Code | Int | 11 | [OECM](OECM.md) |  | `0` = Invalid<br>`1` = GEN<br>`2` = EET<br>`3` = CFDI<br>`4` = FPA<br>`5` = MTD<br>`6` = EWB<br>`7` = PEPPOL<br>`8` = HOI<br>`9` = MYF<br>`10` = EIS<br>`11` = IIS<br>`12` = IIS_ANNUAL<br>`13` = DIGIPOORT<br>`14` = E-Books<br>`15` = DOX<br>`16` = RTIE<br>`17` = E-Billing<br>`18` = Tax Service<br>`19` = AFE<br>`20` = Document Signature<br>`21` = KSeF<br>`22` = GSTReturn<br>`23` = PT Document Signature<br>`24` = Skat DK<br>`25` = EII<br>`26` = NFe<br>`27` = PT eInvoicing<br>`28` = PT Electronic Communications<br>`29` = Veri*factu<br>`30` = BAS<br>`31` = PDF with XML Attachment<br>`32` = FReINV<br>`33` = euBP<br>`34` = ILOI<br>`35` = EDGT<br>`36` = EDCR<br>`37` = NAV |
| 3 | `Priority` | Determination Priority | Int | 11 | - |  |  |
| 4 | `BPCode` | Customer/Vendor Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 5 | `Country` | Country/Region | nVarChar | 3 | [OCRY](OCRY.md) |  |  |
| 6 | `Serie` | Digital Series | Int | 11 | [NNM1](NNM1.md) | -1 |  |
| 7 | `DocType` | Document Type | nVarChar | 20 | - | -1 | `18` = A/P Invoice<br>`19` = A/P Credit Memo<br>`204` = A/P Down Payment<br>`163` = A/P Correction Invoice<br>`164` = A/P Correction Invoice Reversal<br>`20` = Goods Receipt PO<br>`21` = Goods Return<br>`24` = Incoming Payment<br>`46` = Outgoing Payment<br>`67` = Inventory Transfers<br>`15` = Deliveries<br>`16` = Returns<br>`14` = A/R Credit Memos<br>`13` = A/R Invoices |
| 8 | `DocSubType` | Document Subtype | nVarChar | 2 | - | -- | `--`<br>`AR` = All A/R Documents<br>`AP` = All A/P Documents |
| 9 | `ExportFmt` | Export Format | Int | 11 | [OLLF](OLLF.md) |  |  |
| 10 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 11 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 12 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 13 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 14 | `LogInstanc` | Log Instance | Int | 6 | - |  |  |
| 15 | `FileNP` | File Name and Path | Text | 16 | - |  |  |
| 16 | `VersionNum` | Version Number | Int | 11 | - |  |  |
| 17 | `EIIAction` | EII Invoice Action | VarChar | 1 | - | S | `S` = Send<br>`D` = Decision |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
