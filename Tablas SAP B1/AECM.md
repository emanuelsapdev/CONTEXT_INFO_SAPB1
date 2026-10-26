# AECM - Electronic Communication Types or Protocols

- **Tabla:** AECM
- **Descripción:** Electronic Communication Types or Protocols
- **Cantidad de campos:** 13
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AECM.html

## Campos (13)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Communication Type or Protocol | Int | 11 | - |  | `0` = Invalid<br>`1` = GEN<br>`2` = EET<br>`3` = CFDI<br>`4` = FPA<br>`5` = MTD<br>`6` = EWB<br>`7` = PEPPOL<br>`8` = HOI<br>`9` = MYF<br>`10` = EIS<br>`11` = IIS<br>`12` = IIS_ANNUAL<br>`13` = DIGIPOORT<br>`14` = E-Books<br>`15` = DOX<br>`16` = RTIE<br>`17` = E-Billing<br>`18` = Tax Service<br>`19` = AFE<br>`20` = Document Signature<br>`21` = KSeF<br>`22` = GSTReturn<br>`23` = PT Document Signature<br>`24` = Skat DK<br>`25` = EII<br>`26` = NFe<br>`27` = PT eInvoicing<br>`28` = PT Electronic Communications<br>`29` = Veri*factu<br>`30` = BAS<br>`31` = PDF with XML Attachment<br>`32` = FReINV<br>`33` = euBP<br>`34` = ILOI<br>`35` = EDGT<br>`36` = EDCR<br>`37` = NAV |
| 2 | `Descr` | Description | nVarChar | 200 | - |  |  |
| 3 | `LogInstanc` | Log Instance | Int | 6 | - |  |  |
| 4 | `UIOrder` | UI Order | Int | 6 | - |  |  |
| 5 | `StrIndex` | String Index | Int | 6 | - |  |  |
| 6 | `IsActive` | Activation of Communication Type or Protocol | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 7 | `LHost` | Background Process Client Machine Name | nVarChar | 254 | - |  |  |
| 8 | `LPID` | Background Process Client Process ID | Int | 11 | - |  |  |
| 9 | `LTimeout` | Validity Time Stamp of Background Process Client Session | nVarChar | 14 | - |  |  |
| 10 | `RHost` | Machine Name Requesting Control of Background eDoc Processing | nVarChar | 254 | - |  |  |
| 11 | `RPID` | Process ID Requesting Control of Background eDoc Processing | Int | 11 | - |  |  |
| 12 | `RTimeout` | Validity Time Stamp of Background Process Client Request | nVarChar | 14 | - |  |  |
| 13 | `IsHidden` | Hide Electronic Protocol on UI Forms | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code, LogInstanc |
