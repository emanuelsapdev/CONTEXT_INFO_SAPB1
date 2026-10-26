# ACH1 - Checks for Payment - Rows - History

- **Tabla:** ACH1
- **Descripción:** Checks for Payment - Rows - History
- **Cantidad de campos:** 22
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ACH1.html

## Campos (22)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `CheckKey` | SBO Internal Key | Int | 11 | [OCHO](OCHO.md) |  |  |
| 2 | `LineId` | Row Number | Int | 11 | - |  |  |
| 3 | `LineDitail` | Row Details | nVarChar | 40 | - |  |  |
| 4 | `LineMoney` | Row Total | Num | 19.6 | - |  |  |
| 5 | `LineCurr` | Row Currency | nVarChar | 3 | - |  |  |
| 6 | `LineAcct` | Row G/L Acct | nVarChar | 15 | - |  |  |
| 7 | `Line_A_C` | G/L Acct/BP Code | VarChar | 1 | - | 0 |  |
| 8 | `Code` | Tax Definition | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 9 | `CredAcct` | Credited Account | nVarChar | 15 | [OACT](OACT.md) |  |  |
| 10 | `TotalLine` | Row Total | Num | 19.6 | - |  |  |
| 11 | `VatPercent` | Tax %: | Num | 19.6 | - |  |  |
| 12 | `UserSign` | User Signature | Int | 6 | [OUSR](OUSR.md) |  |  |
| 13 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 14 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 57 |  |
| 15 | `LineMnyLC` | Row Total (LC) | Num | 19.6 | - |  |  |
| 16 | `LineMnySC` | Row Total (SC) | Num | 19.6 | - |  |  |
| 17 | `LineMnyFC` | Row Total (FC) | Num | 19.6 | - |  |  |
| 18 | `TotLineLC` | Row Total (LC) | Num | 19.6 | - |  |  |
| 19 | `TotLineSC` | Row Total (SC) | Num | 19.6 | - |  |  |
| 20 | `TotLineFC` | Row Total (FC) | Num | 19.6 | - |  |  |
| 21 | `UserSign2` | Updating User - History | Int | 6 | [OUSR](OUSR.md) |  |  |
| 22 | `UpdateDate` | Date of Update - History | Date | 8 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | CheckKey, LineId, LogInstanc |
