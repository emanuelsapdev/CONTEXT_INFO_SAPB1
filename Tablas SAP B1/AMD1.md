# AMD1 - Amout Differences Report Lines

- **Tabla:** AMD1
- **Descripción:** Amout Differences Report Lines
- **Cantidad de campos:** 16
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/AMD1.html

## Campos (16)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `LineNum` | Internal ID | Int | 11 | - |  |  |
| 2 | `PmnNum` | Payment Number | Int | 11 | [ORCT](ORCT.md) |  |  |
| 3 | `PmnInvID` | Invoice Seq. No. in Payment | Int | 11 | - |  |  |
| 4 | `PmnDate` | Payment Date | Date | 8 | - |  |  |
| 5 | `CardCode` | BP Code | nVarChar | 15 | [OCRD](OCRD.md) |  |  |
| 6 | `InvType` | Invoice Category | nVarChar | 20 | - | 13 | `13` = Sales Invoice |
| 7 | `InvEntry` | Invoice Key | Int | 11 | [OINV](OINV.md) |  |  |
| 8 | `InstId` | Installment ID | Int | 6 | - |  |  |
| 9 | `InvTransID` | Invoice Transaction Number | Int | 11 | [OJDT](OJDT.md) |  |  |
| 10 | `FCCurrency` | Foreign Currency | nVarChar | 3 | [OCRN](OCRN.md) |  |  |
| 11 | `InvRate` | Rate, Invoice | Num | 19.6 | - |  |  |
| 12 | `PmnRate` | Rate, Payment | Num | 19.6 | - |  |  |
| 13 | `Approved` | Confirmed | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 14 | `AmountDiff` | Amount Difference (LC) | Num | 19.6 | - |  |  |
| 15 | `TaxAmtDiff` | Tax Difference (LC) | Num | 19.6 | - |  |  |
| 16 | `TMP_JE` | Temporary Transaction ID | nVarChar | 50 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | LineNum, PmnNum, PmnInvID |
