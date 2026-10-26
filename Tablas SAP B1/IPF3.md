# IPF3 - Landed Costs - Customs Summary

- **Tabla:** IPF3
- **Descripción:** Landed Costs - Customs Summary
- **Cantidad de campos:** 15
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/IPF3.html

## Campos (15)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Landed Costs Internal ID | Int | 11 | [OIPF](OIPF.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `Dscription` | Summary Description | nVarChar | 200 | - |  |  |
| 4 | `LaCAllcAcc` | Landed Costs Alloc. Account | nVarChar | 15 | - |  |  |
| 5 | `CustSum` | Customs Summary | Num | 19.6 | - |  |  |
| 6 | `CustSumFC` | Customs Summary FC | Num | 19.6 | - |  |  |
| 7 | `CustSumSC` | Customs Summary SC | Num | 19.6 | - |  |  |
| 8 | `OpenSum` | Open Customs Summary | Num | 19.6 | - |  |  |
| 9 | `OpenSumFC` | Open Customs Summary (FC) | Num | 19.6 | - |  |  |
| 10 | `OpenSumSC` | Open Customs Summary (SC) | Num | 19.6 | - |  |  |
| 11 | `AccType` | Type of Account of Summarized | Int | 11 | - |  |  |
| 12 | `VatGroup` | VAT Code | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 13 | `CstmVatStk` | Is Customs VAT in Stock | VarChar | 1 | - | Y | `Y` = Yes<br>`N` = No |
| 14 | `CCDEntry` | CCD Abs. Entry | Int | 11 | - |  |  |
| 15 | `LineNum2` | Row Number in IPF2 | Int | 11 | [IPF2](IPF2.md) |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum |
