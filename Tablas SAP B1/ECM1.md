# ECM1 - Parameters for Various Types of Electronic Communication

- **Tabla:** ECM1
- **Descripción:** Parameters for Various Types of Electronic Communication
- **Cantidad de campos:** 16
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ECM1.html

## Campos (16)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Code` | Code | Int | 11 | [OECM](OECM.md) |  | `0` = Invalid<br>`1` = GEN<br>`2` = EET<br>`3` = CFDI<br>`4` = FPA<br>`5` = MTD<br>`6` = EWB<br>`7` = PEPPOL<br>`8` = HOI<br>`9` = MYF<br>`10` = EIS<br>`11` = IIS<br>`12` = IIS_ANNUAL<br>`13` = DIGIPOORT<br>`14` = E-Books<br>`15` = DOX<br>`16` = RTIE<br>`17` = E-Billing<br>`18` = Tax Service<br>`19` = AFE<br>`20` = Document Signature<br>`21` = KSeF<br>`22` = GSTReturn<br>`23` = PT Document Signature<br>`24` = Skat DK<br>`25` = EII<br>`26` = NFe<br>`27` = PT eInvoicing<br>`28` = PT Electronic Communications<br>`29` = Veri*factu<br>`30` = BAS<br>`31` = PDF with XML Attachment<br>`32` = FReINV<br>`33` = euBP<br>`34` = ILOI<br>`35` = EDGT<br>`36` = EDCR<br>`37` = NAV |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `StrIndex` | String Index | Int | 6 | - |  |  |
| 4 | `BPLId` | Branch ID | Int | 11 | [OBPL](OBPL.md) | -1 |  |
| 5 | `ParamType` | Parameter Type | nVarChar | 2 | - | TX | `TX` = General Text<br>`TT` = Title<br>`EM` = E-Mail<br>`UR` = URI Address<br>`SA` = Server Address<br>`PT` = Path<br>`FN` = File Name<br>`LG` = Logic Value - Yes/No<br>`NI` = Number - Integer<br>`NR` = Number - Real<br>`PW` = Password<br>`OT` = Other<br>`MP` = Mapping<br>`GT` = Generation Type<br>`CT` = Certificate<br>`UQ` = User Queries Category<br>`CB` = Combo Box<br>`SP` = Separator<br>`EF` = External Function<br>`IU` = B1i Server URL<br>`NM` = Money<br>`LT` = Long General Text |
| 6 | `ParamVisib` | Parameter is Visible | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 7 | `ParamName` | Parameter Name | nVarChar | 100 | - |  |  |
| 8 | `ParamValue` | Parameter Value | Text | 16 | - |  |  |
| 9 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 10 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 11 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |
| 12 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 13 | `LogInstanc` | Log Instance | Int | 6 | - |  |  |
| 14 | `ParamPrms` | Parameter Parameters | nVarChar | 254 | - |  |  |
| 15 | `UIorder` | UI Order | Int | 6 | - |  |  |
| 16 | `Type` | UI Type | Int | 6 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Code, BPLId, LineNum |
| PARAM_NAME | Yes | Code, BPLId, ParamName |
