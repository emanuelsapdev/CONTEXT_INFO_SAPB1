# SRT1 - Korean Summary Report - Rows1

- **Tabla:** SRT1
- **Descripción:** Korean Summary Report - Rows1
- **Cantidad de campos:** 6
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SRT1.html

## Campos (6)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SumRptId` | Summary Rpt ID | nVarChar | 100 | - |  |  |
| 2 | `SeqNo` | Sequence Number | Int | 11 | - |  |  |
| 3 | `CardNum` | Business Partner Total Numbers | Int | 11 | - |  |  |
| 4 | `TransNum` | Total Trans Number Under BP | Int | 11 | - |  |  |
| 5 | `BaseAmt` | Total Base Amount Under BPs | Num | 19.6 | - |  |  |
| 6 | `TaxAmt` | Total Tax Amount Under BPs | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SumRptId, SeqNo |
