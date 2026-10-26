# OBTC - Internal Bank Operation Codes

- **Tabla:** OBTC
- **Descripción:** Internal Bank Operation Codes
- **Cantidad de campos:** 17
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBTC.html

## Campos (17)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal Number | Int | 11 | - | 0 |  |
| 2 | `InOpCode` | Internal Bank Operation Code Name | nVarChar | 15 | - |  |  |
| 3 | `PstTrans` | Posting Transaction | VarChar | 1 | - | 1 | `1` = Bank Transfer<br>`2` = Incoming Bill of Exchange<br>`3` = Outgoing Bill of Exchange<br>`4` = Outgoing Checks<br>`5` = Deposit |
| 4 | `BPorAct` | BP or Account | VarChar | 1 | - | C | `C` = BP<br>`A` = Account |
| 5 | `PstMethod` | BP Posting Method | VarChar | 1 | - | C | `A` = G/L Account from/to Bank Account<br>`C` = Business Partner from/to Bank Account<br>`J` = Bank Interim Account from/to Bank Account<br>`E` = External Reconciliation<br>`I` = Ignore |
| 6 | `ActFee` | Account Fee | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 7 | `ProjFee` | Project Fee | nVarChar | 20 | [OPRJ](OPRJ.md) |  |  |
| 8 | `PrftCntFee` | Fee Distribution Rule | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 9 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 10 | `UpdateDate` | Date of Update | Date | 8 | - |  |  |
| 11 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 12 | `Descript` | Operation Description | nVarChar | 40 | - |  |  |
| 13 | `PrftCntFe2` | Fee Distribution Rule2 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 14 | `PrftCntFe3` | Fee Distribution Rule3 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 15 | `PrftCntFe4` | Fee Distribution Rule4 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 16 | `PrftCntFe5` | Fee Distribution Rule5 | nVarChar | 8 | [OOCR](OOCR.md) |  |  |
| 17 | `UserSign2` | Updating User | Int | 6 | [OUSR](OUSR.md) |  |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry |
| CODE_NAME | Yes | InOpCode |
