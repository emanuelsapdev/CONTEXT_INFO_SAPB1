# ONNM - Document Numbering

- **Tabla:** ONNM
- **Descripción:** Document Numbering
- **Cantidad de campos:** 10
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ONNM.html

## Campos (10)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ObjectCode` | Document | nVarChar | 20 | - |  |  |
| 2 | `AutoKey` | Automatic Key | Int | 11 | - | 0 |  |
| 3 | `DfltSeries` | Default Series | Int | 11 | - | 0 |  |
| 4 | `UpdCounter` | Update Counter | Int | 11 | - | 0 |  |
| 5 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 6 | `DocSubType` | Document Sub-Type | nVarChar | 2 | - | -- | `--`<br>`IE` = Invoice Exempt<br>`DN` = Debit Memo<br>`IB` = Bill<br>`EB` = Exempt Bill<br>`RI` = Reserve Invoice<br>`IR` = Invoice & Receipt<br>`DM` = A/P Debit Memo<br>`IX` = Export Invoice<br>`RP` = A/P Reserve Invoice<br>`OV` = Outgoing VAT - Withholding Tax<br>`OG` = Outgoing Gross Income - Withholding Tax<br>`ON` = Outgoing Income - Withholding Tax<br>`OS` = Outgoing Social Security - Withholding Tax<br>`OI` = Outgoing Industry Specific - Withholding Tax<br>`OD` = Outgoing District Specific - Withholding Tax<br>`IC` = Incoming WTax Certificate<br>`GA` = GST Tax Invoice<br>`GD` = GST Debit Memo<br>`RV` = Refund Voucher |
| 7 | `DocAlias` | Alternative Document Name | nVarChar | 20 | - |  |  |
| 8 | `PeriodTyp` | Seq. Period Type of Supply Code | VarChar | 1 | - |  |  |
| 9 | `logInstanc` | Log Instance - History | Int | 11 | - |  |  |
| 10 | `DigManuSer` | Digital Manual Series | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ObjectCode, DocSubType |
