# ARC5 - Reciept log vat adjustment-History

- **Tabla:** ARC5
- **Descripción:** Reciept log vat adjustment-History
- **Cantidad de campos:** 26
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/ARC5.html

## Campos (26)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocNum` | Document No. - History | Int | 11 | [ORCT](ORCT.md) |  |  |
| 2 | `InvEntry` | Invoice Key - History | Int | 11 | [OINV](OINV.md) |  |  |
| 3 | `LineNum` | Row Number - History | Int | 11 | - |  |  |
| 4 | `ObjType` | Object Type - History | nVarChar | 20 | [ADP1](ADP1.md) |  |  |
| 5 | `LogInstanc` | Log Instance - History | Int | 11 | - | 0 |  |
| 6 | `VatGroup` | Tax Group - History | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 7 | `VatPrcnt` | Tax % - History | Num | 19.6 | - |  |  |
| 8 | `VatSum` | Tax Amount - History | Num | 19.6 | - |  |  |
| 9 | `BaseSum` | Base Amount - History | Num | 19.6 | - |  |  |
| 10 | `NoDedSum` | Non-Deductible Amount | Num | 19.6 | - |  |  |
| 11 | `BaseSumFc` | Base Amount (FC) | Num | 19.6 | - |  |  |
| 12 | `VatSumFc` | Tax Amount (FC) | Num | 19.6 | - |  |  |
| 13 | `NoDedSumFc` | Non-Deductible Amount (FC) | Num | 19.6 | - |  |  |
| 14 | `BaseSumSc` | Base Amount (SC) | Num | 19.6 | - |  |  |
| 15 | `NoDedSumSc` | Non-Deductible Amount (SC) | Num | 19.6 | - |  |  |
| 16 | `VatSumSc` | VAT Amount (SC) | Num | 19.6 | - |  |  |
| 17 | `CashDiscAc` | Cash Discount Account | nVarChar | 15 | - |  |  |
| 18 | `BaseObjArr` | Base Object Array Number | Int | 6 | - | 1 |  |
| 19 | `BaseObj` | Base Object | Int | 11 | - | 13 |  |
| 20 | `InstlmntId` | Installment ID | Int | 6 | - | 0 |  |
| 21 | `GroupNum` | Group Number | Int | 11 | - | 0 |  |
| 22 | `LineSeq` | Row Sequence | Int | 11 | - | -1 |  |
| 23 | `EquVatPer` | Equalization Tax % | Num | 19.6 | - |  |  |
| 24 | `EquVatSum` | Total Equalization Tax | Num | 19.6 | - |  |  |
| 25 | `EquVatSumF` | Total Equalization Tax (FC) | Num | 19.6 | - |  |  |
| 26 | `EquVatSumS` | Total Equalization Tax (SC) | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocNum, LineSeq, ObjType, LogInstanc |
