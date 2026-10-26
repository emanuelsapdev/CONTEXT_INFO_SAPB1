# SRT2 - Korean Summary Report - Rows2

- **Tabla:** SRT2
- **Descripción:** Korean Summary Report - Rows2
- **Cantidad de campos:** 9
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/SRT2.html

## Campos (9)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `SumRptId` | Summary Rpt ID | nVarChar | 100 | - |  |  |
| 2 | `SeqNo` | Sequence Number | Int | 11 | - |  |  |
| 3 | `VATRegNum` | VAT Reg. Number of BP | nVarChar | 12 | - |  |  |
| 4 | `CardCode` | BP Code on OCRD | nVarChar | 15 | - |  |  |
| 5 | `CardName` | BP Name | nVarChar | 200 | - |  |  |
| 6 | `TransNo` | Total Trans Number under BP | Int | 11 | - |  |  |
| 7 | `BaseAmt` | Total Base Amount under BP | Num | 19.6 | - |  |  |
| 8 | `TaxAmt` | Total Tax Amount under BP | Num | 19.6 | - |  |  |
| 9 | `Remark` | Line Item Remark, do not use | nVarChar | 100 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | SumRptId, SeqNo |
