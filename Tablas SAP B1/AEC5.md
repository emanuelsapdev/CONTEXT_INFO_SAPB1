# AEC5 - List of Canceled Reconciliations for Actions in Electronic Communication

- **Tabla:** AEC5
- **Descripción:** List of Canceled Reconciliations for Actions in Electronic Communication
- **Cantidad de campos:** 14
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AEC5.html

## Campos (14)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal ID | Int | 11 | [ECM2](ECM2.md) |  |  |
| 2 | `LogNum` | Log Number | Int | 11 | - |  |  |
| 3 | `DocType` | Document Type | Int | 11 | - |  |  |
| 4 | `DocAbs` | Document Abs. Entry | Int | 11 | - |  |  |
| 5 | `DocNum` | Document Number | Int | 11 | - |  |  |
| 6 | `UUID` | UUID | nVarChar | 50 | - |  |  |
| 7 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 8 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 9 | `CreateTS` | Create Time - Incl. Sec. | Int | 11 | - |  |  |
| 10 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 11 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 12 | `UpdateTS` | Update Time - Incl. Sec. | Int | 11 | - |  |  |
| 13 | `LogInstanc` | Log Instance | Int | 6 | - |  |  |
| 14 | `Code` | Communication Type or Protocol | Int | 11 | - |  | `0` = Invalid<br>`1` = GEN<br>`2` = EET<br>`3` = CFDI<br>`4` = FPA<br>`5` = MTD<br>`6` = EWB<br>`7` = PEPPOL<br>`8` = HOI<br>`9` = MYF<br>`10` = EIS<br>`11` = IIS<br>`12` = IIS_ANNUAL<br>`13` = DIGIPOORT<br>`14` = E-Books<br>`15` = DOX<br>`16` = RTIE<br>`17` = E-Billing<br>`18` = Tax Service<br>`19` = AFE<br>`20` = Doc. Sign.<br>`21` = KSeF<br>`22` = GSTReturn<br>`23` = PT Doc. Sign.<br>`24` = Skat DK<br>`25` = EII<br>`26` = NFe<br>`27` = PT eInvoicing<br>`28` = PT Electronic Communications<br>`29` = Veri*factu<br>`30` = BAS<br>`31` = PDF with XML Attachment<br>`32` = FReINV<br>`33` = euBP<br>`34` = ILOI<br>`35` = EDGT<br>`36` = EDCR<br>`37` = NAV |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LogNum, LogInstanc |
