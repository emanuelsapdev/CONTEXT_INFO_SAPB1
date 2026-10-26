# MIV3 - Grouped Tax Rows of MI

- **Tabla:** MIV3
- **Descripción:** Grouped Tax Rows of MI
- **Cantidad de campos:** 14
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/MIV3.html

## Campos (14)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `Entry` | Monthly Invoice Entry | Int | 11 | [OMIV](OMIV.md) |  |  |
| 2 | `TaxCode` | Tax Code | nVarChar | 8 | - |  |  |
| 3 | `VatPercent` | VAT Percent | Num | 19.6 | - |  |  |
| 4 | `CrditDebit` | Credit or Debit Transaction | VarChar | 1 | - |  | `C` = Credit<br>`D` = Debit |
| 5 | `BaseSum` | Base Sum | Num | 19.6 | - |  |  |
| 6 | `BaseSumSc` | Base Sum (SC) | Num | 19.6 | - |  |  |
| 7 | `BaseSumFc` | Base Sum (FC) | Num | 19.6 | - |  |  |
| 8 | `VatSum` | VAT Sum | Num | 19.6 | - |  |  |
| 9 | `VatSumSc` | VAT Sum (SC) | Num | 19.6 | - |  |  |
| 10 | `VatSumFc` | VAT Sum (FC) | Num | 19.6 | - |  |  |
| 11 | `TODedBaseS` | Tax Only Deducted Base Sum | Num | 19.6 | - |  |  |
| 12 | `TODedBaSSC` | Tax Only Deducted Base Sum (SC) | Num | 19.6 | - |  |  |
| 13 | `TODedBaSFC` | Tax Only Deducted Base Sum (FC) | Num | 19.6 | - |  |  |
| 14 | `LnDataNum` | Row Number in Tax Data | Int | 11 | - | -1 |  |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | Entry, LnDataNum |
