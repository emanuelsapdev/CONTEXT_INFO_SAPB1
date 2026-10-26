# RRR15 - A/R Return Request - Drawn Dpm Applied

- **Tabla:** RRR15
- **Descripción:** A/R Return Request - Drawn Dpm Applied
- **Cantidad de campos:** 84
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/RRR15.html

## Campos (84)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [ORRR](ORRR.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `ObjType` | object type | nVarChar | 20 | [ADP1](ADP1.md) | 234000031 |  |
| 4 | `LogInstanc` | Log Instance | Int | 11 | - | 0 |  |
| 5 | `VatGroup` | VAT Group Code | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 6 | `StaCode` | Tax Authority Code | nVarChar | 8 | - |  |  |
| 7 | `StaType` | Tax Authority Type | Int | 11 | - |  |  |
| 8 | `StaIndex` | Tax Authority Seq Index | Int | 11 | - |  |  |
| 9 | `BaseNet` | Net LC | Num | 19.6 | - |  |  |
| 10 | `BaseNetFc` | Net FC | Num | 19.6 | - |  |  |
| 11 | `BaseNetSc` | Net SC | Num | 19.6 | - |  |  |
| 12 | `VatSum` | Tax LC | Num | 19.6 | - |  |  |
| 13 | `VatSumFc` | Tax FC | Num | 19.6 | - |  |  |
| 14 | `VatSumSc` | Tax SC | Num | 19.6 | - |  |  |
| 15 | `DctSum` | Deductible Sum LC | Num | 19.6 | - |  |  |
| 16 | `DctSumFc` | Deductible Sum FC | Num | 19.6 | - |  |  |
| 17 | `DctSumSc` | Deductible Sum SC | Num | 19.6 | - |  |  |
| 18 | `EqSum` | Equalization Sum LC | Num | 19.6 | - |  |  |
| 19 | `EqSumFc` | Equalization Sum FC | Num | 19.6 | - |  |  |
| 20 | `EqSumSc` | Equalization Sum SC | Num | 19.6 | - |  |  |
| 21 | `ApplNet` | Applied Net LC | Num | 19.6 | - |  |  |
| 22 | `ApplNetFc` | Applied Net FC | Num | 19.6 | - |  |  |
| 23 | `ApplNetSc` | Applied Net SC | Num | 19.6 | - |  |  |
| 24 | `ApplVat` | Applied Tax LC | Num | 19.6 | - |  |  |
| 25 | `ApplVatFc` | Applied Tax FC | Num | 19.6 | - |  |  |
| 26 | `ApplVatSc` | Applied Tax SC | Num | 19.6 | - |  |  |
| 27 | `ApplDct` | Applied Deductible Sum LC | Num | 19.6 | - |  |  |
| 28 | `ApplDctFc` | Applied Deductible Sum FC | Num | 19.6 | - |  |  |
| 29 | `ApplDctSc` | Applied Deductible Sum SC | Num | 19.6 | - |  |  |
| 30 | `ApplEq` | Applied Equalization Sum LC | Num | 19.6 | - |  |  |
| 31 | `ApplEqFc` | Applied Equalization Sum FC | Num | 19.6 | - |  |  |
| 32 | `ApplEqSc` | Applied Equalization Sum SC | Num | 19.6 | - |  |  |
| 33 | `PaidNet` | Paid Net LC | Num | 19.6 | - |  |  |
| 34 | `PaidNetFc` | Paid Net FC | Num | 19.6 | - |  |  |
| 35 | `PaidNetSc` | Paid Net SC | Num | 19.6 | - |  |  |
| 36 | `PaidVat` | Paid Tax LC | Num | 19.6 | - |  |  |
| 37 | `PaidVatFc` | Paid Tax FC | Num | 19.6 | - |  |  |
| 38 | `PaidVatSc` | Paid Tax SC | Num | 19.6 | - |  |  |
| 39 | `PaidDct` | Paid Deductible Sum LC | Num | 19.6 | - |  |  |
| 40 | `PaidDctFc` | Paid Deductible Sum FC | Num | 19.6 | - |  |  |
| 41 | `PaidDctSc` | Paid Deductible Sum SC | Num | 19.6 | - |  |  |
| 42 | `PaidEq` | Paid Equalization Sum LC | Num | 19.6 | - |  |  |
| 43 | `PaidEqFc` | Paid Equalization Sum FC | Num | 19.6 | - |  |  |
| 44 | `PaidEqSc` | Paid Equalization Sum SC | Num | 19.6 | - |  |  |
| 45 | `DpApplNet` | Dpm Appl Net LC | Num | 19.6 | - |  |  |
| 46 | `DpApplNetF` | Dpm Appl Net FC | Num | 19.6 | - |  |  |
| 47 | `DpApplNetS` | Dpm Appl Net SC | Num | 19.6 | - |  |  |
| 48 | `DpApplVat` | Dpm Appl Tax LC | Num | 19.6 | - |  |  |
| 49 | `DpApplVatF` | Dpm Appl Tax FC | Num | 19.6 | - |  |  |
| 50 | `DpApplVatS` | Dpm Appl Tax SC | Num | 19.6 | - |  |  |
| 51 | `DpApplDct` | Dpm Appl Deductible Sum LC | Num | 19.6 | - |  |  |
| 52 | `DpApplDctF` | Dpm Appl Deductible Sum FC | Num | 19.6 | - |  |  |
| 53 | `DpApplDctS` | Dpm Appl Deductible Sum SC | Num | 19.6 | - |  |  |
| 54 | `DpApplEq` | Dpm Appl Equalization Sum LC | Num | 19.6 | - |  |  |
| 55 | `DpApplEqFc` | Dpm Appl Equalization Sum FC | Num | 19.6 | - |  |  |
| 56 | `DpApplEqSc` | Dpm Appl Equalization Sum SC | Num | 19.6 | - |  |  |
| 57 | `TaxCode` | Tax Code | nVarChar | 8 | [OSTC](OSTC.md) |  |  |
| 58 | `LineType` | Row Type | VarChar | 1 | - | D | `D` = Document<br>`R` = Exchange Rate Rounding<br>`H` = Document Header Rounding |
| 59 | `BaseGrs` | Gross LC | Num | 19.6 | - |  |  |
| 60 | `BaseGrsFc` | Gross FC | Num | 19.6 | - |  |  |
| 61 | `BaseGrsSc` | Gross SC | Num | 19.6 | - |  |  |
| 62 | `ApplGrs` | Applied Gross LC | Num | 19.6 | - |  |  |
| 63 | `ApplGrsFc` | Applied Gross FC | Num | 19.6 | - |  |  |
| 64 | `ApplGrsSc` | Applied Gross SC | Num | 19.6 | - |  |  |
| 65 | `PaidGrs` | Paid Gross LC | Num | 19.6 | - |  |  |
| 66 | `PaidGrsFc` | Paid Gross FC | Num | 19.6 | - |  |  |
| 67 | `PaidGrsSc` | Paid Gross SC | Num | 19.6 | - |  |  |
| 68 | `DpApplGrs` | Dpm Appl Gross LC | Num | 19.6 | - |  |  |
| 69 | `DpApplGrsF` | Dpm Appl Gross FC | Num | 19.6 | - |  |  |
| 70 | `DpApplGrsS` | Dpm Appl Gross SC | Num | 19.6 | - |  |  |
| 71 | `RvsChrgSum` | Reverse Charge Sum | Num | 19.6 | - |  |  |
| 72 | `RvsChrgSc` | Reverse Charge Sum (SC) | Num | 19.6 | - |  |  |
| 73 | `RvsChrgFc` | Reverse Charge Sum (FC) | Num | 19.6 | - |  |  |
| 74 | `ApplRvs` | Applied Reverse Charge Sum LC | Num | 19.6 | - |  |  |
| 75 | `ApplRvsSc` | Applied Reverse Charge Sum SC | Num | 19.6 | - |  |  |
| 76 | `ApplRvsFc` | Applied Reverse Charge Sum FC | Num | 19.6 | - |  |  |
| 77 | `PaidRvs` | Paid Reverse Charge Sum LC | Num | 19.6 | - |  |  |
| 78 | `PaidRvsSc` | Paid Reverse Charge Sum SC | Num | 19.6 | - |  |  |
| 79 | `PaidRvsFc` | Paid Reverse Charge Sum FC | Num | 19.6 | - |  |  |
| 80 | `DpApplRvs` | Dpm Applied Reverse Charge LC | Num | 19.6 | - |  |  |
| 81 | `DpApplRvsS` | Dpm Applied Reverse Charge SC | Num | 19.6 | - |  |  |
| 82 | `DpApplRvsF` | Dpm Applied Reverse Charge FC | Num | 19.6 | - |  |  |
| 83 | `IsPrscGood` | Is Prescribed Goods | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 84 | `IsCstmAct` | Apply Customer Accounting Tax Rule | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum |
