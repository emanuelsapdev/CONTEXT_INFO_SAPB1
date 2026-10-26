# BOE1 - Bill of Exchange for Payment - Rows

- **Tabla:** BOE1
- **Descripción:** Bill of Exchange for Payment - Rows
- **Cantidad de campos:** 14
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/BOE1.html

## Campos (14)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `BoeKey` | SBO Internal Key | Int | 11 | [OBOE](OBOE.md) |  |  |
| 2 | `LineId` | Row No. | Int | 11 | - |  |  |
| 3 | `LineDitail` | Row Details | nVarChar | 40 | - |  |  |
| 4 | `LineMoney` | Row Total | Num | 19.6 | - |  |  |
| 5 | `LineCurr` | Row Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 6 | `LineAcct` | Row Account | nVarChar | 15 | - |  |  |
| 7 | `Line_A_C` | BP/Account | VarChar | 1 | - | 0 |  |
| 8 | `Code` | Tax Definition | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 9 | `CredAcct` | Credited Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 10 | `TotalLine` | Row Total | Num | 19.6 | - |  |  |
| 11 | `VatPercent` | Tax %: | Num | 19.6 | - |  |  |
| 12 | `UserSign` | User Signature | Int | 11 | [OUSR](OUSR.md) |  |  |
| 13 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 14 | `EncryptIV` | Encrypt IV | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | BoeKey, LineId |
