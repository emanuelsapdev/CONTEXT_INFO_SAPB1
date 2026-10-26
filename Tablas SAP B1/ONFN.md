# ONFN - Nota Fiscal Numbering

- **Tabla:** ONFN
- **Descripción:** Nota Fiscal Numbering
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ONFN.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `ObjectCode` | Document | nVarChar | 20 | - |  |  |
| 2 | `AutoKey` | Automatic Key | Int | 11 | - | 0 |  |
| 3 | `DfltSeq` | Default Sequence | Int | 6 | - | 0 |  |
| 4 | `UpdCounter` | Update Counter | Int | 6 | - | 0 |  |
| 5 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 6 | `DocSubType` | Document Sub-Type | nVarChar | 2 | - | -- | `--`<br>`GA` = GST Tax Invoice<br>`GD` = GST Debit Memo<br>`RV` = Refund Voucher |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | ObjectCode, DocSubType |
