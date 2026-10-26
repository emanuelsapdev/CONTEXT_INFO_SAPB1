# INV11 - A/R Invoice - Drawn Dpm Detail

- **Tabla:** INV11
- **Descripción:** A/R Invoice - Drawn Dpm Detail
- **Cantidad de campos:** 70
- **Fuente:** https://help.sap.com/doc/089315d8d0f8475a9fc84fb919b501a3/10.0/en-US/SDKHelp/INV11.html

## Campos (70)

| # | Campo | Descripción | Tipo | Tamaño | Relacionada | Valor por defecto | Valores válidos (Constraints) |
|---|---|---|---|---|---|---|---|
| 1 | `DocEntry` | Document Internal ID | Int | 11 | [OINV](OINV.md) |  |  |
| 2 | `LineNum` | Row Number | Int | 11 | - |  |  |
| 3 | `LineSeq` | Sequence Number | Int | 11 | - |  |  |
| 4 | `BaseAbs` | Base Document Internal ID | Int | 11 | [ODPI](ODPI.md) | -1 |  |
| 5 | `BaseType` | Base Object Type | Int | 11 | - | 203 | `203` = A/R Down Payment |
| 6 | `VatGroup` | VAT Group Code | nVarChar | 8 | [OVTG](OVTG.md) |  |  |
| 7 | `VatPrcnt` | VAT Percent | Num | 19.6 | - |  |  |
| 8 | `LineTotal` | Net LC | Num | 19.6 | - |  |  |
| 9 | `TotalFrgn` | Net FC | Num | 19.6 | - |  |  |
| 10 | `TotalSumSy` | Net SC | Num | 19.6 | - |  |  |
| 11 | `VatSum` | Tax LC | Num | 19.6 | - |  |  |
| 12 | `VatSumFrgn` | Tax FC | Num | 19.6 | - |  |  |
| 13 | `VatSumSys` | Tax SC | Num | 19.6 | - |  |  |
| 14 | `ObjType` | Object Type | nVarChar | 20 | [ADP1](ADP1.md) | 13 |  |
| 15 | `LogInstanc` | Log Instance | Int | 11 | - |  |  |
| 16 | `IsAcq` | Acquisition Tax Liable | VarChar | 1 | - | N | `N` = No<br>`Y` = Yes |
| 17 | `IsAllDrawn` | Remaining Amount Drawn | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 18 | `IsGross` | Is Gross Line | VarChar | 1 | - | N | `N` = Net Line<br>`Y` = Gross Line |
| 19 | `Gross` | Gross LC | Num | 19.6 | - |  |  |
| 20 | `GrossFc` | Gross FC | Num | 19.6 | - |  |  |
| 21 | `GrossSc` | Gross SC | Num | 19.6 | - |  |  |
| 22 | `ApplNet` | Applied Net LC | Num | 19.6 | - |  |  |
| 23 | `ApplNetFc` | Applied Net FC | Num | 19.6 | - |  |  |
| 24 | `ApplNetSc` | Applied Net SC | Num | 19.6 | - |  |  |
| 25 | `ApplVat` | Applied Tax LC | Num | 19.6 | - |  |  |
| 26 | `ApplVatFc` | Applied Tax FC | Num | 19.6 | - |  |  |
| 27 | `ApplVatSc` | Applied Tax SC | Num | 19.6 | - |  |  |
| 28 | `BaseNet` | Base Net LC | Num | 19.6 | - |  |  |
| 29 | `BaseNetFc` | Base Net FC | Num | 19.6 | - |  |  |
| 30 | `BaseNetSc` | Base Net SC | Num | 19.6 | - |  |  |
| 31 | `BaseVat` | Base Tax LC | Num | 19.6 | - |  |  |
| 32 | `BaseVatFc` | Base Tax FC | Num | 19.6 | - |  |  |
| 33 | `BaseVatSc` | Base Tax SC | Num | 19.6 | - |  |  |
| 34 | `BaseGross` | Base Gross LC | Num | 19.6 | - |  |  |
| 35 | `BaseGrossF` | Base Gross FC | Num | 19.6 | - |  |  |
| 36 | `BaseGrossS` | Base Gross SC | Num | 19.6 | - |  |  |
| 37 | `LineType` | Line Type | VarChar | 1 | - | D | `D` = Document Row<br>`R` = Currency Rounding<br>`H` = Down Payment Document Rounding |
| 38 | `DctSum` | Deductible Sum LC | Num | 19.6 | - |  |  |
| 39 | `DctSumFc` | Deductible Sum FC | Num | 19.6 | - |  |  |
| 40 | `DctSumSc` | Deductible Sum SC | Num | 19.6 | - |  |  |
| 41 | `EqSum` | Equalization Sum LC | Num | 19.6 | - |  |  |
| 42 | `EqSumFc` | Equalization Sum FC | Num | 19.6 | - |  |  |
| 43 | `EqSumSc` | Equalization Sum SC | Num | 19.6 | - |  |  |
| 44 | `ApplDct` | Applied Deductible Sum LC | Num | 19.6 | - |  |  |
| 45 | `ApplDctFc` | Applied Deductible Sum FC | Num | 19.6 | - |  |  |
| 46 | `ApplDctSc` | Applied Deductible Sum SC | Num | 19.6 | - |  |  |
| 47 | `ApplEq` | Applied Equalization Sum LC | Num | 19.6 | - |  |  |
| 48 | `ApplEqFc` | Applied Equalization Sum FC | Num | 19.6 | - |  |  |
| 49 | `ApplEqSc` | Applied Equalization Sum SC | Num | 19.6 | - |  |  |
| 50 | `BaseDct` | Base Deductible Sum LC | Num | 19.6 | - |  |  |
| 51 | `BaseDctFc` | Base Deductible Sum FC | Num | 19.6 | - |  |  |
| 52 | `BaseDctSc` | Base Deductible Sum SC | Num | 19.6 | - |  |  |
| 53 | `BaseEq` | Base Equalization Sum LC | Num | 19.6 | - |  |  |
| 54 | `BaseEqFc` | Base Equalization Sum FC | Num | 19.6 | - |  |  |
| 55 | `BaseEqSc` | Base Equalization Sum SC | Num | 19.6 | - |  |  |
| 56 | `TaxCode` | Tax Code | nVarChar | 8 | [OSTC](OSTC.md) |  |  |
| 57 | `ApplGross` | Applied Gross LC | Num | 19.6 | - |  |  |
| 58 | `ApplGrossF` | Applied Gross FC | Num | 19.6 | - |  |  |
| 59 | `ApplGrossS` | Applied Gross SC | Num | 19.6 | - |  |  |
| 60 | `TaxAdjust` | Manual Tax Adjustment | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |
| 61 | `RvsChrgSum` | Reverse Charge Sum LC | Num | 19.6 | - |  |  |
| 62 | `RvsChrgFc` | Reverse Charge Sum FC | Num | 19.6 | - |  |  |
| 63 | `RvsChrgSc` | Reverse Charge Sum SC | Num | 19.6 | - |  |  |
| 64 | `BasRvsChrg` | Base Reverse Charge LC | Num | 19.6 | - |  |  |
| 65 | `BasRvsFc` | Base Reverse Charge FC | Num | 19.6 | - |  |  |
| 66 | `BasRvsSc` | Base Reverse Charge SC | Num | 19.6 | - |  |  |
| 67 | `ApplRvs` | Applied Reverse Charge LC | Num | 19.6 | - |  |  |
| 68 | `ApplRvsFc` | Applied Reverse Charge FC | Num | 19.6 | - |  |  |
| 69 | `ApplRvsSc` | Applied Reverse Charge SC | Num | 19.6 | - |  |  |
| 70 | `IsCstmAct` | Apply Customer Accounting Tax Rule | VarChar | 1 | - | N | `Y` = Yes<br>`N` = No |

## Claves e índices (1)

| Clave / Índice | Única | Campos |
|---|---|---|
| PRIMARY | Yes | DocEntry, LineNum, LineSeq |
