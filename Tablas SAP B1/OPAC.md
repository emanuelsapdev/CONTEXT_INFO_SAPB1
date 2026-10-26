# OPAC - PAC Companies

- **Tabla:** OPAC
- **Descripción:** PAC Companies
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OPAC.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `PACCode` | PAC Code | nVarChar | 16 | - |  |  |
| 2 | `PACName` | PAC Name | nVarChar | 100 | - |  |  |
| 3 | `PublicKey` | PAC Public Key | Text | 16 | - |  |  |
| 4 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 5 | `LogInstanc` | Log Instance | Int | 11 | - |  |  |
| 6 | `EDFCode` | Communication Type or Protocol | Int | 11 | - |  | `0` = Invalid<br>`1` = GEN<br>`2` = EET<br>`3` = CFDI<br>`4` = FPA<br>`5` = MTD<br>`6` = EWB<br>`7` = PEPPOL<br>`8` = HOI<br>`9` = MYF<br>`10` = EIS<br>`11` = IIS<br>`12` = IIS_ANNUAL |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | PACCode |
