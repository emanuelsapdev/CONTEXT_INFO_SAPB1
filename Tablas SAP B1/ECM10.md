# ECM10 - Emergency Number

- **Tabla:** ECM10
- **Descripción:** Emergency Number
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ECM10.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal ID | Int | 11 | - |  |  |
| 2 | `Number` | Emergency Number | nVarChar | 50 | - |  |  |
| 3 | `Code` | Code | Int | 11 | [OECM](OECM.md) |  | `0` = Invalid<br>`1` = GEN<br>`2` = EET<br>`3` = CFDI<br>`4` = FPA<br>`5` = MTD<br>`6` = EWB<br>`7` = PEPPOL<br>`8` = HOI<br>`9` = MYF<br>`10` = EIS<br>`11` = IIS<br>`12` = IIS_ANNUAL<br>`13` = DIGIPOORT<br>`14` = E-Books<br>`15` = DOX<br>`16` = RTIE<br>`17` = E-Billing<br>`18` = Tax Service<br>`19` = AFE<br>`20` = Document Signature<br>`21` = KSeF<br>`22` = GSTReturn<br>`23` = PT Document Signature<br>`24` = Skat DK<br>`25` = EII<br>`26` = NFe<br>`27` = PT eInvoicing<br>`28` = PT Electronic Communications<br>`29` = Veri*factu<br>`30` = BAS<br>`31` = PDF with XML Attachment<br>`32` = FReINV<br>`33` = euBP<br>`34` = ILOI<br>`35` = EDGT<br>`36` = EDCR<br>`37` = NAV |
| 4 | `Status` | Status | VarChar | 1 | - | N | `N` = New<br>`U` = Used<br>`E` = Expired |
| 5 | `UserSign` | User Signature | Int | 6 | - |  |  |
| 6 | `CreateDate` | Creation Date | Date | 8 | - |  |  |
| 7 | `CreateTS` | Creation Time - Incl. Secs | Int | 11 | - |  |  |
| 8 | `UserSign2` | Updating User | Int | 6 | - |  |  |
| 9 | `UpdateDate` | Update Date | Date | 8 | - |  |  |
| 10 | `UpdateTS` | Update Time - Incl. Secs | Int | 11 | - |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| NUMBER | Yes | Code, Number |
