# OBTD - Journal Vouchers List

- **Tabla:** OBTD
- **Descripción:** Journal Vouchers List
- **Cantidad de campos:** 12
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/OBTD.html

## Campos (12)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `BatchNum` | Journal Voucher No. | Int | 11 | - |  |  |
| 2 | `Status` | Open/Closed Document | VarChar | 1 | - | O | `O` = Open<br>`C` = Closed |
| 3 | `NumOfTrans` | No. of Transactions | Int | 6 | - |  |  |
| 4 | `DateID` | Posting Date | Date | 8 | - |  |  |
| 5 | `LocTotal` | Total (LC) | Num | 19.6 | - |  |  |
| 6 | `FcTotal` | Total (FC) | Num | 19.6 | - |  |  |
| 7 | `SysTotal` | Total (SC) | Num | 19.6 | - |  |  |
| 8 | `MemoID` | Details | nVarChar | 50 | - |  |  |
| 9 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 10 | `Remarks` | Journal Voucher Remarks Field | nVarChar | 50 | - |  |  |
| 11 | `UpdateTS` | Update Full Time | Int | 11 | - |  |  |
| 12 | `DataVers` | Data Version | Int | 11 | - | 1 |  |

## Claves e índices (2)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | BatchNum |
| STATUS | No | Status |
