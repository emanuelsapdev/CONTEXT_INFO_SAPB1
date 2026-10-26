# TAX2 - VAT Transactions - Grouped Rows

- **Tabla:** TAX2
- **Descripción:** VAT Transactions - Grouped Rows
- **Cantidad de campos:** 18
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/TAX2.html

## Campos (18)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `AbsEntry` | Internal ID | Int | 11 | [OTAX](OTAX.md) |  |  |
| 2 | `LineSeq` | Row Sequence | Int | 11 | - |  |  |
| 3 | `TaxCode` | Tax Code | nVarChar | 8 | - |  |  |
| 4 | `VatPercent` | VAT Percent | Num | 19.6 | - |  |  |
| 5 | `CrditDebit` | Credit or Debit Transaction | VarChar | 1 | - |  | `C` = Credit<br>`D` = Debit |
| 6 | `BaseSum` | Base Sum | Num | 19.6 | - |  |  |
| 7 | `BaseSumSc` | Base Sum (SC) | Num | 19.6 | - |  |  |
| 8 | `BaseSumFc` | Base Sum (FC) | Num | 19.6 | - |  |  |
| 9 | `VatSum` | VAT Sum | Num | 19.6 | - |  |  |
| 10 | `VatSumSc` | VAT Sum (SC) | Num | 19.6 | - |  |  |
| 11 | `VatSumFc` | VAT Sum (FC) | Num | 19.6 | - |  |  |
| 12 | `TODedBaseS` | Tax Only Deducted Base Sum | Num | 19.6 | - |  |  |
| 13 | `TODedBaSSC` | Tax Only Deducted Base Sum (SC) | Num | 19.6 | - |  |  |
| 14 | `TODedBaSFC` | Tax Only Deducted Base Sum (FC) | Num | 19.6 | - |  |  |
| 15 | `LnDataNum` | Row Number in Tax Data | Int | 11 | - | -1 |  |
| 16 | `DeductSum` | Deduct VAT Sum | Num | 19.6 | - |  |  |
| 17 | `DedctSumSC` | Deduct VAT Sum (SC) | Num | 19.6 | - |  |  |
| 18 | `DedctSumFC` | Deduct VAT Sum (FC) | Num | 19.6 | - |  |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | AbsEntry, LineSeq |
